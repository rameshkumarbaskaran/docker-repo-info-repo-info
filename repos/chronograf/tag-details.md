<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `chronograf`

-	[`chronograf:1.10`](#chronograf110)
-	[`chronograf:1.10-alpine`](#chronograf110-alpine)
-	[`chronograf:1.10.1`](#chronograf1101)
-	[`chronograf:1.10.1-alpine`](#chronograf1101-alpine)
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
$ docker pull chronograf@sha256:7f70b698b16019da2081e439e60d388d897d07ea3239a8eb2b447b36d4ae68e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:1575b03b10ca5ccf30556eea9dbd26982e1a99d692d5de81f0377d84c8a91438
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82803422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054a06db258d36e98f5dc5ae85d5a8d56fde1d3ea6097bb7a5ac4c7f3251bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:59 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 23 Mar 2023 06:12:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:12:06 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:12:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:12:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b38a80a9c9f14745c5d3c39eca2ab0731ac3ad6e829bda6ab0ba1876fa33b2`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 5.2 MB (5226171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1b6422de45b88751631cd54d00aa6d1c9874585581faddd81344f0acf2f5`  
		Last Modified: Thu, 23 Mar 2023 06:13:08 GMT  
		Size: 46.1 MB (46141452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685b83b562e36e2face4136733838671e6425ac7f52a0d3016937da2327e260b`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af80511b750f16f6e44c34b5cf5820739dd58ba881371c8486917b9e1f2f47d7`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144629686b91940362645ae1fa7bf7ebbf5121109839bebd74562587534c1931`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6b9f4671b3a38e24c8201ed17383d01c548363ceb7fc439d52a6bc62eeea2b8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74943607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62c2d779c052a262520ffbf9be366f982bf04faacf1d581bfe80ea0823c6216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:19:37 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:19:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:19:47 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:47 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e2d1fb361ebdda9db81728e80176f6f474bdf5c10f69d22a9bc7cf1fbcd3e`  
		Last Modified: Mon, 20 Mar 2023 23:20:32 GMT  
		Size: 4.5 MB (4491674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9b8290f36c18a224dce91891da05be44b6b042414268f80ee85f12bf9f0c68`  
		Last Modified: Mon, 20 Mar 2023 23:21:07 GMT  
		Size: 43.9 MB (43850247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e287c4a6bebbf849894dbc6a5fd310a5cb013767e7916197741da84207ff984`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ba9667bd632fdb8c76cabfc13bc6cf4f76fe122404b61c148b648b9b92a1a`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d676056e39bdee28d29406d65cc80daff8d2ad59b155b20db267ed722fbb3d52`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:98f5092a4721f125c30ee1ab2103bf85b0750685e7fe0039522430846b446897
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7f68f45a4146dd20662f47184472490a17057514c93c981702b24c43380795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:48:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:48:28 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 23 Mar 2023 06:48:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:34 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:34 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6205390f4cee9baf3d57184932d7c6ca7f58e6136c1763f534eb08225e247`  
		Last Modified: Thu, 23 Mar 2023 06:48:56 GMT  
		Size: 5.2 MB (5209241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057d1883ded49f4d97633e0533d479c4f32a3bbe010f9e38aa632848a236e7fe`  
		Last Modified: Thu, 23 Mar 2023 06:49:21 GMT  
		Size: 43.9 MB (43854710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e29410c4026f0a9dcfec5d1ba20ddabe993e79551b70cb073a4859a5619d8d`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811c8ed96d158eda707b73a7b9383861629da8374a5ab036a9d12912430d199`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d4f4aae88dec4eb87906d22474b4c7686c61850280d36376425adecc646022`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10-alpine`

```console
$ docker pull chronograf@sha256:d37ff2dd6017f2f23c2451e4714f58ec128c40d913cdddc2474dd5e80ce9d02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:423c00ce3340d6bf56476c306bbf92b373723c282878cff0402170666094777c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31471055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234348391f7544b632a053deb2f795217fbd8442889a0b694f35147d68b77717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:33:03 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:33:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:33:08 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:33:08 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:33:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:33:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538a64e1ef5dbe8fb18e216fd54e05f520792ec5fc4e57ed6784c270f23123b`  
		Last Modified: Mon, 20 Mar 2023 23:35:05 GMT  
		Size: 27.8 MB (27787107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4aa26f9e765988bebf28ad457129c10c32c67a6721431d8d8db4b6d3ec9e5`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168433b6bec0615f392cf522b6e2e55bae37e7b25eaa9d30d35e5990d004b6b2`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3931308a86c84cc296410b2d724b21967ed4929e7b812b8126e1a58bc61822`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.1`

```console
$ docker pull chronograf@sha256:7f70b698b16019da2081e439e60d388d897d07ea3239a8eb2b447b36d4ae68e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.1` - linux; amd64

```console
$ docker pull chronograf@sha256:1575b03b10ca5ccf30556eea9dbd26982e1a99d692d5de81f0377d84c8a91438
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82803422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054a06db258d36e98f5dc5ae85d5a8d56fde1d3ea6097bb7a5ac4c7f3251bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:59 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 23 Mar 2023 06:12:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:12:06 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:12:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:12:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b38a80a9c9f14745c5d3c39eca2ab0731ac3ad6e829bda6ab0ba1876fa33b2`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 5.2 MB (5226171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1b6422de45b88751631cd54d00aa6d1c9874585581faddd81344f0acf2f5`  
		Last Modified: Thu, 23 Mar 2023 06:13:08 GMT  
		Size: 46.1 MB (46141452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685b83b562e36e2face4136733838671e6425ac7f52a0d3016937da2327e260b`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af80511b750f16f6e44c34b5cf5820739dd58ba881371c8486917b9e1f2f47d7`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144629686b91940362645ae1fa7bf7ebbf5121109839bebd74562587534c1931`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.1` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6b9f4671b3a38e24c8201ed17383d01c548363ceb7fc439d52a6bc62eeea2b8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74943607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62c2d779c052a262520ffbf9be366f982bf04faacf1d581bfe80ea0823c6216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:19:37 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:19:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:19:47 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:47 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e2d1fb361ebdda9db81728e80176f6f474bdf5c10f69d22a9bc7cf1fbcd3e`  
		Last Modified: Mon, 20 Mar 2023 23:20:32 GMT  
		Size: 4.5 MB (4491674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9b8290f36c18a224dce91891da05be44b6b042414268f80ee85f12bf9f0c68`  
		Last Modified: Mon, 20 Mar 2023 23:21:07 GMT  
		Size: 43.9 MB (43850247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e287c4a6bebbf849894dbc6a5fd310a5cb013767e7916197741da84207ff984`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ba9667bd632fdb8c76cabfc13bc6cf4f76fe122404b61c148b648b9b92a1a`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d676056e39bdee28d29406d65cc80daff8d2ad59b155b20db267ed722fbb3d52`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.10.1` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:98f5092a4721f125c30ee1ab2103bf85b0750685e7fe0039522430846b446897
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7f68f45a4146dd20662f47184472490a17057514c93c981702b24c43380795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:48:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:48:28 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 23 Mar 2023 06:48:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:34 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:34 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6205390f4cee9baf3d57184932d7c6ca7f58e6136c1763f534eb08225e247`  
		Last Modified: Thu, 23 Mar 2023 06:48:56 GMT  
		Size: 5.2 MB (5209241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057d1883ded49f4d97633e0533d479c4f32a3bbe010f9e38aa632848a236e7fe`  
		Last Modified: Thu, 23 Mar 2023 06:49:21 GMT  
		Size: 43.9 MB (43854710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e29410c4026f0a9dcfec5d1ba20ddabe993e79551b70cb073a4859a5619d8d`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811c8ed96d158eda707b73a7b9383861629da8374a5ab036a9d12912430d199`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d4f4aae88dec4eb87906d22474b4c7686c61850280d36376425adecc646022`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.10.1-alpine`

```console
$ docker pull chronograf@sha256:d37ff2dd6017f2f23c2451e4714f58ec128c40d913cdddc2474dd5e80ce9d02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.10.1-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:423c00ce3340d6bf56476c306bbf92b373723c282878cff0402170666094777c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31471055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234348391f7544b632a053deb2f795217fbd8442889a0b694f35147d68b77717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:33:03 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:33:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:33:08 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:33:08 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:33:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:33:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538a64e1ef5dbe8fb18e216fd54e05f520792ec5fc4e57ed6784c270f23123b`  
		Last Modified: Mon, 20 Mar 2023 23:35:05 GMT  
		Size: 27.8 MB (27787107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4aa26f9e765988bebf28ad457129c10c32c67a6721431d8d8db4b6d3ec9e5`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168433b6bec0615f392cf522b6e2e55bae37e7b25eaa9d30d35e5990d004b6b2`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3931308a86c84cc296410b2d724b21967ed4929e7b812b8126e1a58bc61822`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7`

```console
$ docker pull chronograf@sha256:850769d852df1b1e92f5e381162aeea7d7c104971cce0cab7c1bffe41616def2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:5d54d6796c7647401174632ba4e8261ff5882d576315ba17486450436cb2967d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70589663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3e032472df72439e6f75d60e6b1d99df1306c92455b287296cc3001ec45d29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:16 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Mar 2023 06:11:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:11:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:11:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:11:25 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:11:25 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:11:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:11:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:11:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5ee2f97013796ca61338dafa41afc07f64d22f87e9f6e30f476e7f1adc1465`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 4.4 MB (4416479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe144243e4e37f784469f1d7abe2f5ed84b457884a4414a08a50d065e667171`  
		Last Modified: Thu, 23 Mar 2023 06:12:26 GMT  
		Size: 34.7 MB (34737380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501659ddede463460d9df1fea8676c1c68e1f2eea571da93540c603dacc53e7`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338cab9a5d9028c6adec3cc2184d2d9e1d612e385073721fe8966fb264e5214d`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3216407121620f08b32c7977c224cae6f8a257923963cb557a6abdafb40a81f`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:94da81418168332b02638f41c85c1e161bf13205d773e6b1d78ead6cdf33e808
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63417783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4ea02c433638716d21710d64b77db3e8f3df3fc7d35a48c7a47096c6278e9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:18:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:18:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:18:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:18:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:18:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:18:59 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:00 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194fc479f85dae216cf633f2d4ffbe817a883893ccabb8d6afcbea26a33b422f`  
		Last Modified: Mon, 20 Mar 2023 23:20:18 GMT  
		Size: 3.7 MB (3719000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb975712f4ade64bc953d6f870bd5a75982458002a12038382c80d70a706c6da`  
		Last Modified: Mon, 20 Mar 2023 23:20:22 GMT  
		Size: 33.1 MB (33097089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fb487f52c56c03152f2fb3c543660067a0cdc2bcb69f34c6829884951ef144`  
		Last Modified: Mon, 20 Mar 2023 23:20:17 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00957939eeebe13c09bff513ca1bf00888773b214e145ccdc08538e83e34db91`  
		Last Modified: Mon, 20 Mar 2023 23:20:17 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e351fea321fe703552781d702331c82741519040053b615b7959e7229a1b6d85`  
		Last Modified: Mon, 20 Mar 2023 23:20:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:73488e91b2a8af5f613853c97aa0b73252ba7989ed2b0589eb454f5ef5707e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67742417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c391f59abec42be37972063184af137c8e0338ed59432ad66dc20e0bf811750`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:47:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:47:58 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Mar 2023 06:48:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:05 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:05 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbff9deb86694cd1d0c537cab95be934769525ff5f9defaf74901935d9a3e4a`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 4.4 MB (4417985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b443e757c5779bdda28a01d9a2d04ec8e73111d5631662a6667b816c67c922eb`  
		Last Modified: Thu, 23 Mar 2023 06:48:48 GMT  
		Size: 33.2 MB (33237334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009c517aa8036ca984b6a0df0d3c995e35179d8a1ec36f9af5168f576bf1819`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a80a6931dbfcaa2311b5db7acdffc7db655f385c20e3428405e9a94eabd874`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4a7b62a074ad95fc90fff989538d387aec811dc51fe6a2aa44df9c1f7e9826`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7-alpine`

```console
$ docker pull chronograf@sha256:43d27f1e43861c40c44a94c2e4e481aeb6b47829d314188c2c1ba75db770c62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:85a4488728aed058eca03f61a31d1b4ecc845eafd5a141ea3efc8c9b558bfde8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23241117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d7af98f11629df7705612e538445d310dfc87a7be38d4d34a5b5f3e492f8e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:32:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:32:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:32:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:07 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:08 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6057f9b5f58aeb57565eb27b1159b26ff6cd718679a91ecbd1589ca6a23543fa`  
		Last Modified: Mon, 20 Mar 2023 23:33:47 GMT  
		Size: 19.6 MB (19557180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fc2f685a7712e6be2dc0e328df9a864ffe51d83d6e418cabf2d0aa0d6cbbe1`  
		Last Modified: Mon, 20 Mar 2023 23:33:45 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c771905dfe5aab5bfb066556b3701c2a1d159660e0ebdbc8bbbc64ee366aed00`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7c79deb8346b260ca40fdde7dda3a3f23daff80149d25ae98d57f75e14d5b9`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17`

```console
$ docker pull chronograf@sha256:850769d852df1b1e92f5e381162aeea7d7c104971cce0cab7c1bffe41616def2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:5d54d6796c7647401174632ba4e8261ff5882d576315ba17486450436cb2967d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70589663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc3e032472df72439e6f75d60e6b1d99df1306c92455b287296cc3001ec45d29`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:16 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Mar 2023 06:11:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:11:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:11:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:11:25 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:11:25 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:11:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:11:25 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:11:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc5ee2f97013796ca61338dafa41afc07f64d22f87e9f6e30f476e7f1adc1465`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 4.4 MB (4416479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fe144243e4e37f784469f1d7abe2f5ed84b457884a4414a08a50d065e667171`  
		Last Modified: Thu, 23 Mar 2023 06:12:26 GMT  
		Size: 34.7 MB (34737380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1501659ddede463460d9df1fea8676c1c68e1f2eea571da93540c603dacc53e7`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338cab9a5d9028c6adec3cc2184d2d9e1d612e385073721fe8966fb264e5214d`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3216407121620f08b32c7977c224cae6f8a257923963cb557a6abdafb40a81f`  
		Last Modified: Thu, 23 Mar 2023 06:12:22 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:94da81418168332b02638f41c85c1e161bf13205d773e6b1d78ead6cdf33e808
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63417783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e4ea02c433638716d21710d64b77db3e8f3df3fc7d35a48c7a47096c6278e9b`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:18:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:18:50 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:18:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:18:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:18:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:18:59 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:00 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:194fc479f85dae216cf633f2d4ffbe817a883893ccabb8d6afcbea26a33b422f`  
		Last Modified: Mon, 20 Mar 2023 23:20:18 GMT  
		Size: 3.7 MB (3719000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb975712f4ade64bc953d6f870bd5a75982458002a12038382c80d70a706c6da`  
		Last Modified: Mon, 20 Mar 2023 23:20:22 GMT  
		Size: 33.1 MB (33097089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78fb487f52c56c03152f2fb3c543660067a0cdc2bcb69f34c6829884951ef144`  
		Last Modified: Mon, 20 Mar 2023 23:20:17 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00957939eeebe13c09bff513ca1bf00888773b214e145ccdc08538e83e34db91`  
		Last Modified: Mon, 20 Mar 2023 23:20:17 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e351fea321fe703552781d702331c82741519040053b615b7959e7229a1b6d85`  
		Last Modified: Mon, 20 Mar 2023 23:20:17 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.7.17` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:73488e91b2a8af5f613853c97aa0b73252ba7989ed2b0589eb454f5ef5707e31
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67742417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c391f59abec42be37972063184af137c8e0338ed59432ad66dc20e0bf811750`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:47:58 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:47:58 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Thu, 23 Mar 2023 06:48:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:05 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:05 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:05 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:05 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:05 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:05 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:05 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bbff9deb86694cd1d0c537cab95be934769525ff5f9defaf74901935d9a3e4a`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 4.4 MB (4417985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b443e757c5779bdda28a01d9a2d04ec8e73111d5631662a6667b816c67c922eb`  
		Last Modified: Thu, 23 Mar 2023 06:48:48 GMT  
		Size: 33.2 MB (33237334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e009c517aa8036ca984b6a0df0d3c995e35179d8a1ec36f9af5168f576bf1819`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72a80a6931dbfcaa2311b5db7acdffc7db655f385c20e3428405e9a94eabd874`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba4a7b62a074ad95fc90fff989538d387aec811dc51fe6a2aa44df9c1f7e9826`  
		Last Modified: Thu, 23 Mar 2023 06:48:45 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.7.17-alpine`

```console
$ docker pull chronograf@sha256:43d27f1e43861c40c44a94c2e4e481aeb6b47829d314188c2c1ba75db770c62b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.7.17-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:85a4488728aed058eca03f61a31d1b4ecc845eafd5a141ea3efc8c9b558bfde8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23241117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4d7af98f11629df7705612e538445d310dfc87a7be38d4d34a5b5f3e492f8e8`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:32:02 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:32:07 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:32:07 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:07 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:07 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:08 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6057f9b5f58aeb57565eb27b1159b26ff6cd718679a91ecbd1589ca6a23543fa`  
		Last Modified: Mon, 20 Mar 2023 23:33:47 GMT  
		Size: 19.6 MB (19557180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76fc2f685a7712e6be2dc0e328df9a864ffe51d83d6e418cabf2d0aa0d6cbbe1`  
		Last Modified: Mon, 20 Mar 2023 23:33:45 GMT  
		Size: 12.3 KB (12260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c771905dfe5aab5bfb066556b3701c2a1d159660e0ebdbc8bbbc64ee366aed00`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 11.9 KB (11894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7c79deb8346b260ca40fdde7dda3a3f23daff80149d25ae98d57f75e14d5b9`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8`

```console
$ docker pull chronograf@sha256:5197a789bac990045fa8825d0ea5cbcd627d02d6553ed152bc823fd67f0f7054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:d5c267ecd20ee2bd410d30c0dc42aa5e37f9b0841b62f5a4a58742b1436eb308
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cd8cc544951fd0ff71fc99961a02c193858b222ac6135c08c38ce029e9b690`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Mar 2023 06:11:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:11:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:11:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:11:43 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:11:43 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:11:43 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:11:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:11:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b38a80a9c9f14745c5d3c39eca2ab0731ac3ad6e829bda6ab0ba1876fa33b2`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 5.2 MB (5226171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39c924992902744aa1e6d0ec24a57c5ceac251cd245c70b048ba493a88a717`  
		Last Modified: Thu, 23 Mar 2023 06:12:39 GMT  
		Size: 34.6 MB (34578976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634ccb6519123dedae91ececd01a0bbfda5c481ef3333f5337214655e3f49ece`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec444031881454f7b613a330771dfc6821a4aef1bdc7029fdea9e7ee8aca7e35`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be954e0035ff49b0ee01cf3ddc26a2b4adcbadbe35740f5bf0a41d3f367d9f56`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6d9a3c92b243886b7e8bf181cecf3649aca7b99d68eee43a0e27cde34eaa06c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63843678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf826eb27aeadfb637fddce65c936a898dbddbd2f908c025dafe8a45a3fc214`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:19:11 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:19:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:19:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:19:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:19:19 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:19 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e2d1fb361ebdda9db81728e80176f6f474bdf5c10f69d22a9bc7cf1fbcd3e`  
		Last Modified: Mon, 20 Mar 2023 23:20:32 GMT  
		Size: 4.5 MB (4491674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a77beb02ec5e0103b02891311b93f6f4100ba27be4d9031042576cae37a50a`  
		Last Modified: Mon, 20 Mar 2023 23:20:35 GMT  
		Size: 32.8 MB (32750315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e648b008cb601df24cb6ee2e5d999c5b68295a79ec6b53eb2edc8121ac7b623`  
		Last Modified: Mon, 20 Mar 2023 23:20:31 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b8c4564d4c120c408b5b685d33f1dd56a7e364e83df74a15d9813643f2103f`  
		Last Modified: Mon, 20 Mar 2023 23:20:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e600194e854255d0977d1078332beff5f1c8be7c9c179d043b82b8e175e56`  
		Last Modified: Mon, 20 Mar 2023 23:20:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7525598b16fab21ab97a8f4843a7fb1ec0dc76ab9e4deccc75c90a9db03c1d5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deafd8b7b9b3a073a15d3a0e653019a13857080a5f2c2e97cf704f02fde1982e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:48:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:48:13 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Mar 2023 06:48:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:19 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:19 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6205390f4cee9baf3d57184932d7c6ca7f58e6136c1763f534eb08225e247`  
		Last Modified: Thu, 23 Mar 2023 06:48:56 GMT  
		Size: 5.2 MB (5209241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ecd033f9f08d263b863dd4f042bb197f0b742fc05fab272e7a21477ab808a`  
		Last Modified: Thu, 23 Mar 2023 06:48:58 GMT  
		Size: 32.6 MB (32643779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef4906841e5f36995499717f83abbb63eddadd52d2b15aa002e4b3d54e520ee`  
		Last Modified: Thu, 23 Mar 2023 06:48:55 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76292d8ca44d7a2ef0c0febfaf13eea78ea7eb4a59e4efd2b030a9f056a5a0e`  
		Last Modified: Thu, 23 Mar 2023 06:48:55 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326fab870fc53113ef51ea6686e65fab2d8cec44b9e1cc555e04e7351b60187`  
		Last Modified: Thu, 23 Mar 2023 06:48:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8-alpine`

```console
$ docker pull chronograf@sha256:013ab68fba3d6e6effed14734b24535bcb55cdc4f944393a8b9ee20703d1c51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:646590b32d7c824292c78a4e2b011b74d41460398c885924e91c35777fba5950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22888148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cc2b92598f1d1e5e5aee4432b1eaf64d7e6ed1299cd3866bd0c4b7ca65f0d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:32:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:32:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:32:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:33 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:33 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c008d7a954acfa200b1c93d31293618a2d229cd0ff85aae946ff9250f77e26`  
		Last Modified: Mon, 20 Mar 2023 23:34:11 GMT  
		Size: 19.2 MB (19204205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b1c7b75e16ff8bc10dba411b00a51a411b02986ed189faec8813413bc1e839`  
		Last Modified: Mon, 20 Mar 2023 23:34:08 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05ae2937daeb9753e7e22400ae64c66b54180e836a6f934401246009f10a55c`  
		Last Modified: Mon, 20 Mar 2023 23:34:08 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ba16ef19fb49700e7489926c02248ba31a29fac9d692f3b20816b74dfcb06d`  
		Last Modified: Mon, 20 Mar 2023 23:34:08 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10`

```console
$ docker pull chronograf@sha256:5197a789bac990045fa8825d0ea5cbcd627d02d6553ed152bc823fd67f0f7054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:d5c267ecd20ee2bd410d30c0dc42aa5e37f9b0841b62f5a4a58742b1436eb308
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71240949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cd8cc544951fd0ff71fc99961a02c193858b222ac6135c08c38ce029e9b690`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:37 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Mar 2023 06:11:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:11:43 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:11:43 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:11:43 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:11:43 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:11:43 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:11:43 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:11:43 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b38a80a9c9f14745c5d3c39eca2ab0731ac3ad6e829bda6ab0ba1876fa33b2`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 5.2 MB (5226171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa39c924992902744aa1e6d0ec24a57c5ceac251cd245c70b048ba493a88a717`  
		Last Modified: Thu, 23 Mar 2023 06:12:39 GMT  
		Size: 34.6 MB (34578976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634ccb6519123dedae91ececd01a0bbfda5c481ef3333f5337214655e3f49ece`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec444031881454f7b613a330771dfc6821a4aef1bdc7029fdea9e7ee8aca7e35`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be954e0035ff49b0ee01cf3ddc26a2b4adcbadbe35740f5bf0a41d3f367d9f56`  
		Last Modified: Thu, 23 Mar 2023 06:12:35 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6d9a3c92b243886b7e8bf181cecf3649aca7b99d68eee43a0e27cde34eaa06c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63843678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf826eb27aeadfb637fddce65c936a898dbddbd2f908c025dafe8a45a3fc214`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:19:11 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:19:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:19:19 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:19:19 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:19:19 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:19 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e2d1fb361ebdda9db81728e80176f6f474bdf5c10f69d22a9bc7cf1fbcd3e`  
		Last Modified: Mon, 20 Mar 2023 23:20:32 GMT  
		Size: 4.5 MB (4491674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a77beb02ec5e0103b02891311b93f6f4100ba27be4d9031042576cae37a50a`  
		Last Modified: Mon, 20 Mar 2023 23:20:35 GMT  
		Size: 32.8 MB (32750315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e648b008cb601df24cb6ee2e5d999c5b68295a79ec6b53eb2edc8121ac7b623`  
		Last Modified: Mon, 20 Mar 2023 23:20:31 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b8c4564d4c120c408b5b685d33f1dd56a7e364e83df74a15d9813643f2103f`  
		Last Modified: Mon, 20 Mar 2023 23:20:31 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5e600194e854255d0977d1078332beff5f1c8be7c9c179d043b82b8e175e56`  
		Last Modified: Mon, 20 Mar 2023 23:20:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.8.10` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:7525598b16fab21ab97a8f4843a7fb1ec0dc76ab9e4deccc75c90a9db03c1d5d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940117 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deafd8b7b9b3a073a15d3a0e653019a13857080a5f2c2e97cf704f02fde1982e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:48:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:48:13 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Thu, 23 Mar 2023 06:48:18 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:18 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:18 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:19 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:19 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:19 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:19 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:19 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6205390f4cee9baf3d57184932d7c6ca7f58e6136c1763f534eb08225e247`  
		Last Modified: Thu, 23 Mar 2023 06:48:56 GMT  
		Size: 5.2 MB (5209241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd0ecd033f9f08d263b863dd4f042bb197f0b742fc05fab272e7a21477ab808a`  
		Last Modified: Thu, 23 Mar 2023 06:48:58 GMT  
		Size: 32.6 MB (32643779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ef4906841e5f36995499717f83abbb63eddadd52d2b15aa002e4b3d54e520ee`  
		Last Modified: Thu, 23 Mar 2023 06:48:55 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76292d8ca44d7a2ef0c0febfaf13eea78ea7eb4a59e4efd2b030a9f056a5a0e`  
		Last Modified: Thu, 23 Mar 2023 06:48:55 GMT  
		Size: 11.9 KB (11908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1326fab870fc53113ef51ea6686e65fab2d8cec44b9e1cc555e04e7351b60187`  
		Last Modified: Thu, 23 Mar 2023 06:48:55 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.8.10-alpine`

```console
$ docker pull chronograf@sha256:013ab68fba3d6e6effed14734b24535bcb55cdc4f944393a8b9ee20703d1c51e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.8.10-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:646590b32d7c824292c78a4e2b011b74d41460398c885924e91c35777fba5950
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22888148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3cc2b92598f1d1e5e5aee4432b1eaf64d7e6ed1299cd3866bd0c4b7ca65f0d4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:32:28 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:32:33 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:32:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:33 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:33 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:33 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c008d7a954acfa200b1c93d31293618a2d229cd0ff85aae946ff9250f77e26`  
		Last Modified: Mon, 20 Mar 2023 23:34:11 GMT  
		Size: 19.2 MB (19204205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60b1c7b75e16ff8bc10dba411b00a51a411b02986ed189faec8813413bc1e839`  
		Last Modified: Mon, 20 Mar 2023 23:34:08 GMT  
		Size: 12.3 KB (12263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e05ae2937daeb9753e7e22400ae64c66b54180e836a6f934401246009f10a55c`  
		Last Modified: Mon, 20 Mar 2023 23:34:08 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ba16ef19fb49700e7489926c02248ba31a29fac9d692f3b20816b74dfcb06d`  
		Last Modified: Mon, 20 Mar 2023 23:34:08 GMT  
		Size: 237.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9`

```console
$ docker pull chronograf@sha256:8dfad8c6fbc0f6f579b909f7115ecbe40ff07cba005e65d8d4f626bfbb4f1bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:8275a47e8954dc9de3421eb12e3caefb95c0d8e05d8a41867b802a34ffe27b72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71888473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267a9bd73fdd1e8c17e24d067bfbd4cde282b2be1fcb589d7d43a71964bcdbd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:48 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Mar 2023 06:11:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:11:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:11:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:11:55 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:11:55 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:11:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:11:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b38a80a9c9f14745c5d3c39eca2ab0731ac3ad6e829bda6ab0ba1876fa33b2`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 5.2 MB (5226171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b1074cfc6898328ebc115273d16edcf708f557d75b47102188683bea317a70`  
		Last Modified: Thu, 23 Mar 2023 06:12:52 GMT  
		Size: 35.2 MB (35226508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894913378309de72c4d5cae996455b7c1e379bdef4512ebd6752b61a3df279b6`  
		Last Modified: Thu, 23 Mar 2023 06:12:48 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a834c2d89c4157fe731213688a8cd8f862d9d835dde017a4252ab0d917a5ef`  
		Last Modified: Thu, 23 Mar 2023 06:12:48 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e612f740fb125f7fdd57accad65147f45c4630aa533ea4f1d6fb033b873bb3`  
		Last Modified: Thu, 23 Mar 2023 06:12:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b49bec8a545eb6a449d2e6543f2e09233875dbaba54706d331a5e1efe1e45c89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64619847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5eec79eca1cc3ad257a65bc1a8d573b01c88cc502f91be226b007fd1537ccc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:19:24 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:19:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:19:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:19:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:19:33 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:33 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e2d1fb361ebdda9db81728e80176f6f474bdf5c10f69d22a9bc7cf1fbcd3e`  
		Last Modified: Mon, 20 Mar 2023 23:20:32 GMT  
		Size: 4.5 MB (4491674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ba8c97a4b3d9c78ec8e6593b433956643d6d83abeb82c5a7ea66e4e404ed1b`  
		Last Modified: Mon, 20 Mar 2023 23:20:51 GMT  
		Size: 33.5 MB (33526475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bec5f5bd6d4e9284d74e5c7ab56405ca7d740e7d581e5c51e34ddf28f21bfb1`  
		Last Modified: Mon, 20 Mar 2023 23:20:47 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6897fa725923c5d7af247610a2caacc38ee5f4215a7b8c381cbeaf3fd2ff7d`  
		Last Modified: Mon, 20 Mar 2023 23:20:47 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d6aca0fd21b5d870e110b1b7268129ba59ee7f0831dc16a128dc926dabddc2`  
		Last Modified: Mon, 20 Mar 2023 23:20:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:28b33a1290f734dc2de22ba3ef73107a96ad5a20ec9433da016961cfc2c172a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68691752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e46747c891b2bdc12b37b1f529af4b0dceccf3a9831949e212f323b18f37546`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:48:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:48:20 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Mar 2023 06:48:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:26 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:26 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6205390f4cee9baf3d57184932d7c6ca7f58e6136c1763f534eb08225e247`  
		Last Modified: Thu, 23 Mar 2023 06:48:56 GMT  
		Size: 5.2 MB (5209241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7c099df12f935f9d8ef60e9e254cfc67a34170e3d3c0e58013c3f7445a6771`  
		Last Modified: Thu, 23 Mar 2023 06:49:09 GMT  
		Size: 33.4 MB (33395421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0800c1ea5b9403bdcc5da9489c9cb543784898c8baaa0127d2dcc082d680ad4`  
		Last Modified: Thu, 23 Mar 2023 06:49:06 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b642f7806bc5e4e852c385e6e285c61aec7408551b7202912b9a24d08d9a53e3`  
		Last Modified: Thu, 23 Mar 2023 06:49:06 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6077948dd3add94577769c391aa7ade91cbe345ffe5daf2d01583d89f4bea81`  
		Last Modified: Thu, 23 Mar 2023 06:49:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9-alpine`

```console
$ docker pull chronograf@sha256:b3f0e2c413f240512110252486a33c5e0a4e4ae973649f6844033c7f65a523cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d500cdd54dc39fdceea4544445036164ab301ee84c40c575b8d8dc00d9dcfe39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23356096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a2abefd191f4e8af62de64e515651f8b5e4277dc3e77d7380d4f9889bbdf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:32:45 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:32:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:32:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:50 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:50 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:50 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4b2b970542af10485588f1c647b88fb9dc862aa3fa4a28fb648068536d9063`  
		Last Modified: Mon, 20 Mar 2023 23:34:34 GMT  
		Size: 19.7 MB (19672150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2869bd41f14acaf178e9b360e0546aa9dc17c88357964159e4928f3c617678`  
		Last Modified: Mon, 20 Mar 2023 23:34:31 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25be3f58aeee1d9224acbfc79c33ed82dacc3ab2c646dee2547951019439ad86`  
		Last Modified: Mon, 20 Mar 2023 23:34:31 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ba192c91c0614c14344f00609a42c362e858ed1139f65b72fe91116c8e76b`  
		Last Modified: Mon, 20 Mar 2023 23:34:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4`

```console
$ docker pull chronograf@sha256:8dfad8c6fbc0f6f579b909f7115ecbe40ff07cba005e65d8d4f626bfbb4f1bea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:8275a47e8954dc9de3421eb12e3caefb95c0d8e05d8a41867b802a34ffe27b72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71888473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:267a9bd73fdd1e8c17e24d067bfbd4cde282b2be1fcb589d7d43a71964bcdbd1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:48 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Mar 2023 06:11:54 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:11:55 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:11:55 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:11:55 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:11:55 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:11:55 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:11:55 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:11:55 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b38a80a9c9f14745c5d3c39eca2ab0731ac3ad6e829bda6ab0ba1876fa33b2`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 5.2 MB (5226171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b1074cfc6898328ebc115273d16edcf708f557d75b47102188683bea317a70`  
		Last Modified: Thu, 23 Mar 2023 06:12:52 GMT  
		Size: 35.2 MB (35226508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894913378309de72c4d5cae996455b7c1e379bdef4512ebd6752b61a3df279b6`  
		Last Modified: Thu, 23 Mar 2023 06:12:48 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22a834c2d89c4157fe731213688a8cd8f862d9d835dde017a4252ab0d917a5ef`  
		Last Modified: Thu, 23 Mar 2023 06:12:48 GMT  
		Size: 11.9 KB (11904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74e612f740fb125f7fdd57accad65147f45c4630aa533ea4f1d6fb033b873bb3`  
		Last Modified: Thu, 23 Mar 2023 06:12:48 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:b49bec8a545eb6a449d2e6543f2e09233875dbaba54706d331a5e1efe1e45c89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64619847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5eec79eca1cc3ad257a65bc1a8d573b01c88cc502f91be226b007fd1537ccc3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:19:24 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:19:32 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:19:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:19:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:19:33 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:33 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:33 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:33 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:33 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e2d1fb361ebdda9db81728e80176f6f474bdf5c10f69d22a9bc7cf1fbcd3e`  
		Last Modified: Mon, 20 Mar 2023 23:20:32 GMT  
		Size: 4.5 MB (4491674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ba8c97a4b3d9c78ec8e6593b433956643d6d83abeb82c5a7ea66e4e404ed1b`  
		Last Modified: Mon, 20 Mar 2023 23:20:51 GMT  
		Size: 33.5 MB (33526475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bec5f5bd6d4e9284d74e5c7ab56405ca7d740e7d581e5c51e34ddf28f21bfb1`  
		Last Modified: Mon, 20 Mar 2023 23:20:47 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6897fa725923c5d7af247610a2caacc38ee5f4215a7b8c381cbeaf3fd2ff7d`  
		Last Modified: Mon, 20 Mar 2023 23:20:47 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d6aca0fd21b5d870e110b1b7268129ba59ee7f0831dc16a128dc926dabddc2`  
		Last Modified: Mon, 20 Mar 2023 23:20:47 GMT  
		Size: 240.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:1.9.4` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:28b33a1290f734dc2de22ba3ef73107a96ad5a20ec9433da016961cfc2c172a1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68691752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e46747c891b2bdc12b37b1f529af4b0dceccf3a9831949e212f323b18f37546`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:48:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:48:20 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Thu, 23 Mar 2023 06:48:26 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:26 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:26 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:26 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:26 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:26 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6205390f4cee9baf3d57184932d7c6ca7f58e6136c1763f534eb08225e247`  
		Last Modified: Thu, 23 Mar 2023 06:48:56 GMT  
		Size: 5.2 MB (5209241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a7c099df12f935f9d8ef60e9e254cfc67a34170e3d3c0e58013c3f7445a6771`  
		Last Modified: Thu, 23 Mar 2023 06:49:09 GMT  
		Size: 33.4 MB (33395421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0800c1ea5b9403bdcc5da9489c9cb543784898c8baaa0127d2dcc082d680ad4`  
		Last Modified: Thu, 23 Mar 2023 06:49:06 GMT  
		Size: 12.2 KB (12246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b642f7806bc5e4e852c385e6e285c61aec7408551b7202912b9a24d08d9a53e3`  
		Last Modified: Thu, 23 Mar 2023 06:49:06 GMT  
		Size: 11.9 KB (11905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6077948dd3add94577769c391aa7ade91cbe345ffe5daf2d01583d89f4bea81`  
		Last Modified: Thu, 23 Mar 2023 06:49:05 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:1.9.4-alpine`

```console
$ docker pull chronograf@sha256:b3f0e2c413f240512110252486a33c5e0a4e4ae973649f6844033c7f65a523cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:1.9.4-alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:d500cdd54dc39fdceea4544445036164ab301ee84c40c575b8d8dc00d9dcfe39
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.4 MB (23356096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e2a2abefd191f4e8af62de64e515651f8b5e4277dc3e77d7380d4f9889bbdf6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:32:45 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:32:50 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:32:50 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:50 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:50 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:50 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:50 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:50 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4b2b970542af10485588f1c647b88fb9dc862aa3fa4a28fb648068536d9063`  
		Last Modified: Mon, 20 Mar 2023 23:34:34 GMT  
		Size: 19.7 MB (19672150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb2869bd41f14acaf178e9b360e0546aa9dc17c88357964159e4928f3c617678`  
		Last Modified: Mon, 20 Mar 2023 23:34:31 GMT  
		Size: 12.3 KB (12266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25be3f58aeee1d9224acbfc79c33ed82dacc3ab2c646dee2547951019439ad86`  
		Last Modified: Mon, 20 Mar 2023 23:34:31 GMT  
		Size: 11.9 KB (11897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce5ba192c91c0614c14344f00609a42c362e858ed1139f65b72fe91116c8e76b`  
		Last Modified: Mon, 20 Mar 2023 23:34:31 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:alpine`

```console
$ docker pull chronograf@sha256:d37ff2dd6017f2f23c2451e4714f58ec128c40d913cdddc2474dd5e80ce9d02c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `chronograf:alpine` - linux; amd64

```console
$ docker pull chronograf@sha256:423c00ce3340d6bf56476c306bbf92b373723c282878cff0402170666094777c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.5 MB (31471055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234348391f7544b632a053deb2f795217fbd8442889a0b694f35147d68b77717`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Mar 2023 23:20:24 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Mon, 20 Mar 2023 23:32:02 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates
# Mon, 20 Mar 2023 23:33:03 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:33:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/chronograf/releases/chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     gpg --batch --verify chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz.asc chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf chronograf-${CHRONOGRAF_VERSION}-static_linux_amd64.tar.gz &&     rm -f /usr/src/chronograf-*/chronograf.conf &&     chmod +x /usr/src/chronograf-*/* &&     cp -a /usr/src/chronograf-*/* /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:33:08 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:33:08 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:33:08 GMT
COPY file:91fe01086b7984524af1eeb6657c6aea15ce5e169fd42a42e1ef2c54374d30a2 in /entrypoint.sh 
# Mon, 20 Mar 2023 23:33:08 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:33:08 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69b7a2cbfc2f3b3305293d689573f3c9651d6053e5f780a9ba42a4c836d8d6c9`  
		Last Modified: Mon, 13 Mar 2023 23:21:18 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb34dde8977f23b1801f384e88a01cdf4a4ecde93bbb69899ab3dbff7700c78b`  
		Last Modified: Mon, 20 Mar 2023 23:33:44 GMT  
		Size: 284.8 KB (284821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7538a64e1ef5dbe8fb18e216fd54e05f520792ec5fc4e57ed6784c270f23123b`  
		Last Modified: Mon, 20 Mar 2023 23:35:05 GMT  
		Size: 27.8 MB (27787107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd4aa26f9e765988bebf28ad457129c10c32c67a6721431d8d8db4b6d3ec9e5`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 12.3 KB (12267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:168433b6bec0615f392cf522b6e2e55bae37e7b25eaa9d30d35e5990d004b6b2`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 11.9 KB (11898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b3931308a86c84cc296410b2d724b21967ed4929e7b812b8126e1a58bc61822`  
		Last Modified: Mon, 20 Mar 2023 23:35:00 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `chronograf:latest`

```console
$ docker pull chronograf@sha256:7f70b698b16019da2081e439e60d388d897d07ea3239a8eb2b447b36d4ae68e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:1575b03b10ca5ccf30556eea9dbd26982e1a99d692d5de81f0377d84c8a91438
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82803422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:054a06db258d36e98f5dc5ae85d5a8d56fde1d3ea6097bb7a5ac4c7f3251bb58`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 01:30:27 GMT
ADD file:60911afdacfdc216e44115addb5f3cc07f4166e8a4adf7be94a58aacc327ad63 in / 
# Thu, 23 Mar 2023 01:30:27 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:11:37 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:11:59 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 23 Mar 2023 06:12:05 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:12:06 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:12:06 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:12:06 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:12:06 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:12:06 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:f1f26f5702560b7e591bef5c4d840f76a232bf13fd5aefc4e22077a1ae4440c7`  
		Last Modified: Thu, 23 Mar 2023 01:34:23 GMT  
		Size: 31.4 MB (31411405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08b38a80a9c9f14745c5d3c39eca2ab0731ac3ad6e829bda6ab0ba1876fa33b2`  
		Last Modified: Thu, 23 Mar 2023 06:12:36 GMT  
		Size: 5.2 MB (5226171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6b1b6422de45b88751631cd54d00aa6d1c9874585581faddd81344f0acf2f5`  
		Last Modified: Thu, 23 Mar 2023 06:13:08 GMT  
		Size: 46.1 MB (46141452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:685b83b562e36e2face4136733838671e6425ac7f52a0d3016937da2327e260b`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af80511b750f16f6e44c34b5cf5820739dd58ba881371c8486917b9e1f2f47d7`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:144629686b91940362645ae1fa7bf7ebbf5121109839bebd74562587534c1931`  
		Last Modified: Thu, 23 Mar 2023 06:13:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm variant v7

```console
$ docker pull chronograf@sha256:6b9f4671b3a38e24c8201ed17383d01c548363ceb7fc439d52a6bc62eeea2b8c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74943607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62c2d779c052a262520ffbf9be366f982bf04faacf1d581bfe80ea0823c6216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 01:57:55 GMT
ADD file:182fe91b8976a8871aba0d2ff9d4400a60317c8dec282261ba94247500c8d3dc in / 
# Wed, 01 Mar 2023 01:57:55 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:19:11 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:19:37 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:19:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:19:47 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:19:47 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:19:47 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:19:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:19:47 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:b4770fcf2ef78c1e46693da734476bfaf03cbe1d0b6e0a0f22c2c2e53419e803`  
		Last Modified: Wed, 01 Mar 2023 02:03:02 GMT  
		Size: 26.6 MB (26577290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f72e2d1fb361ebdda9db81728e80176f6f474bdf5c10f69d22a9bc7cf1fbcd3e`  
		Last Modified: Mon, 20 Mar 2023 23:20:32 GMT  
		Size: 4.5 MB (4491674 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b9b8290f36c18a224dce91891da05be44b6b042414268f80ee85f12bf9f0c68`  
		Last Modified: Mon, 20 Mar 2023 23:21:07 GMT  
		Size: 43.9 MB (43850247 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e287c4a6bebbf849894dbc6a5fd310a5cb013767e7916197741da84207ff984`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 12.2 KB (12249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b0ba9667bd632fdb8c76cabfc13bc6cf4f76fe122404b61c148b648b9b92a1a`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d676056e39bdee28d29406d65cc80daff8d2ad59b155b20db267ed722fbb3d52`  
		Last Modified: Mon, 20 Mar 2023 23:21:01 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `chronograf:latest` - linux; arm64 variant v8

```console
$ docker pull chronograf@sha256:98f5092a4721f125c30ee1ab2103bf85b0750685e7fe0039522430846b446897
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7f68f45a4146dd20662f47184472490a17057514c93c981702b24c43380795`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:48:13 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 23 Mar 2023 06:48:28 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Thu, 23 Mar 2023 06:48:34 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Thu, 23 Mar 2023 06:48:34 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Thu, 23 Mar 2023 06:48:34 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Thu, 23 Mar 2023 06:48:34 GMT
EXPOSE 8888
# Thu, 23 Mar 2023 06:48:34 GMT
VOLUME [/var/lib/chronograf]
# Thu, 23 Mar 2023 06:48:35 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Thu, 23 Mar 2023 06:48:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 23 Mar 2023 06:48:35 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfc6205390f4cee9baf3d57184932d7c6ca7f58e6136c1763f534eb08225e247`  
		Last Modified: Thu, 23 Mar 2023 06:48:56 GMT  
		Size: 5.2 MB (5209241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057d1883ded49f4d97633e0533d479c4f32a3bbe010f9e38aa632848a236e7fe`  
		Last Modified: Thu, 23 Mar 2023 06:49:21 GMT  
		Size: 43.9 MB (43854710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85e29410c4026f0a9dcfec5d1ba20ddabe993e79551b70cb073a4859a5619d8d`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5811c8ed96d158eda707b73a7b9383861629da8374a5ab036a9d12912430d199`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0d4f4aae88dec4eb87906d22474b4c7686c61850280d36376425adecc646022`  
		Last Modified: Thu, 23 Mar 2023 06:49:16 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
