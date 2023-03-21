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
$ docker pull chronograf@sha256:3e3e6978901d5091c39e2cd8438fac8767b1db617169e881c94ff9fe5ccb45e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10` - linux; amd64

```console
$ docker pull chronograf@sha256:c0ab4053aba5da7bbe55c35abd5184117a0ee9146155b112404e3e2329f273a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82803459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e8332c725f9d526950f495821bee19fc234d603ad6102fa8ced1c9c6a6b95a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:32:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:32:53 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:32:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:32:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:59 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:59 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:33:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:33:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:33:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fbae0f9b7314139fc8cf586a274e59efd4bab289f8c70f51de567fd49e2c4`  
		Last Modified: Mon, 20 Mar 2023 23:33:56 GMT  
		Size: 5.2 MB (5226242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337a768d84760225d90be0f3e833e89225e0387799cdc04019a8a7a0bc54e99a`  
		Last Modified: Mon, 20 Mar 2023 23:34:49 GMT  
		Size: 46.1 MB (46141408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959c874c2f7f1c46b96b10658e6ae9a641c1296501ef204cb5ddafa29033bb22`  
		Last Modified: Mon, 20 Mar 2023 23:34:43 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62ea9549eea35393a5f46ef374c9787a4eecf9c5b85ba384c92f545cac0ba76`  
		Last Modified: Mon, 20 Mar 2023 23:34:43 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6263d6fa9c8c2ce72bb2b95f624fbf746bbdb6b68cfe2c1bb14087911d63fb85`  
		Last Modified: Mon, 20 Mar 2023 23:34:44 GMT  
		Size: 240.0 B  
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
$ docker pull chronograf@sha256:d1306cd7d2003990a8228c85cc092841f4c1569e432c76546f82fef363581d01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6937b7c88a5861070c99f0d7f9fa747da4503cc1b3634ca849625ab5b59da555`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:40:06 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:40:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:40:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:40:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:40:14 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:40:14 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:40:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:40:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:40:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ac30e8757d0417421968a74cf9d8352c11cef6e9a94f8086b189076f4bb999`  
		Last Modified: Mon, 20 Mar 2023 23:40:40 GMT  
		Size: 5.2 MB (5209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1822cac3aa5821565094fbcf277937f8fba866c6702ad0fa77fc2f46f7a925d3`  
		Last Modified: Mon, 20 Mar 2023 23:41:06 GMT  
		Size: 43.9 MB (43854681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d030f0702d70868441768ad3edcdec05d93cd10056556f129b5c2785407d79`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b39f86ccdb7ca8aade7d10e09ee8718dfe19693fa53e3d4c1721404dd4b2b9`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb045b7a48f0a73099313d3eee8c52df4dd478d79907253f6bd796d3906222`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
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
$ docker pull chronograf@sha256:3e3e6978901d5091c39e2cd8438fac8767b1db617169e881c94ff9fe5ccb45e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.10.1` - linux; amd64

```console
$ docker pull chronograf@sha256:c0ab4053aba5da7bbe55c35abd5184117a0ee9146155b112404e3e2329f273a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82803459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e8332c725f9d526950f495821bee19fc234d603ad6102fa8ced1c9c6a6b95a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:32:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:32:53 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:32:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:32:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:59 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:59 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:33:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:33:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:33:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fbae0f9b7314139fc8cf586a274e59efd4bab289f8c70f51de567fd49e2c4`  
		Last Modified: Mon, 20 Mar 2023 23:33:56 GMT  
		Size: 5.2 MB (5226242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337a768d84760225d90be0f3e833e89225e0387799cdc04019a8a7a0bc54e99a`  
		Last Modified: Mon, 20 Mar 2023 23:34:49 GMT  
		Size: 46.1 MB (46141408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959c874c2f7f1c46b96b10658e6ae9a641c1296501ef204cb5ddafa29033bb22`  
		Last Modified: Mon, 20 Mar 2023 23:34:43 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62ea9549eea35393a5f46ef374c9787a4eecf9c5b85ba384c92f545cac0ba76`  
		Last Modified: Mon, 20 Mar 2023 23:34:43 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6263d6fa9c8c2ce72bb2b95f624fbf746bbdb6b68cfe2c1bb14087911d63fb85`  
		Last Modified: Mon, 20 Mar 2023 23:34:44 GMT  
		Size: 240.0 B  
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
$ docker pull chronograf@sha256:d1306cd7d2003990a8228c85cc092841f4c1569e432c76546f82fef363581d01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6937b7c88a5861070c99f0d7f9fa747da4503cc1b3634ca849625ab5b59da555`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:40:06 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:40:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:40:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:40:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:40:14 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:40:14 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:40:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:40:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:40:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ac30e8757d0417421968a74cf9d8352c11cef6e9a94f8086b189076f4bb999`  
		Last Modified: Mon, 20 Mar 2023 23:40:40 GMT  
		Size: 5.2 MB (5209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1822cac3aa5821565094fbcf277937f8fba866c6702ad0fa77fc2f46f7a925d3`  
		Last Modified: Mon, 20 Mar 2023 23:41:06 GMT  
		Size: 43.9 MB (43854681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d030f0702d70868441768ad3edcdec05d93cd10056556f129b5c2785407d79`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b39f86ccdb7ca8aade7d10e09ee8718dfe19693fa53e3d4c1721404dd4b2b9`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb045b7a48f0a73099313d3eee8c52df4dd478d79907253f6bd796d3906222`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
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
$ docker pull chronograf@sha256:c4f0b9edc02602dff01de00ef82040402a6a0472289b3b05d02ff91524d1880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7` - linux; amd64

```console
$ docker pull chronograf@sha256:e2c0fdc4b23b10f87ab9e5c9617d1d035619117fab9dc7159f5ac7431fdefef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70589888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3363732a6c900845ecb011e33d91c62c5204787e64cac44ef62a20bca72f711a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:31:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:31:48 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:31:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:31:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:31:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:31:57 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:31:57 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:31:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:31:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:31:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c975e472544cfef3b1edb65cbba179cddff2a74f36ae6256e4c207282315d63`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 4.4 MB (4416570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c10bc705875c556e87ee3caa63c1aa6c63043d84e145a0c757f4afd6d574a8`  
		Last Modified: Mon, 20 Mar 2023 23:33:35 GMT  
		Size: 34.7 MB (34737512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebda569ad94c5137c57fafa4e571228c87b3cec5d0dd44169bc7add5ad7e8d0`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807dd9bb835ad8734aa84d019b96f2587d54ac55219cf08664b3b15c3b6de6e2`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed53773262e6cc5a3a1e85d72db687fbcd6305f0f288c81927f1aab51961cfa`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:3fc023fc5ab29b474f349b7f0442179a4dd1655af686fddffb26427125d85197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67742600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc7d2cc708a431e1376870d18cbbf655ef11b1fe31a7ed2a31abb4d58bc7e6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:39:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:39:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:39:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:39:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:39:33 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:39:34 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:39:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:39:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:39:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ce4cbf4c5b42ca7aa605b687581c08ee9d305bec441f2d66bae7e12c74e66d`  
		Last Modified: Mon, 20 Mar 2023 23:40:28 GMT  
		Size: 4.4 MB (4418049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9d9259d6017680ecb29212efc19f0b6f032c3ab955cb055992407e4bfbd3a2`  
		Last Modified: Mon, 20 Mar 2023 23:40:31 GMT  
		Size: 33.2 MB (33237338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a671a717b998aea3a2e768f65c029688aa5ec5c08d2614c1d15acb09015b921`  
		Last Modified: Mon, 20 Mar 2023 23:40:27 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746a063ad5ee911421b2327bb41984d6caed6d0627902bcc3fc5134051b4f47d`  
		Last Modified: Mon, 20 Mar 2023 23:40:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83093168381990146209da7573d0c3320f0479aced5bac134ced76b6a17d47c4`  
		Last Modified: Mon, 20 Mar 2023 23:40:27 GMT  
		Size: 240.0 B  
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
$ docker pull chronograf@sha256:c4f0b9edc02602dff01de00ef82040402a6a0472289b3b05d02ff91524d1880c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.7.17` - linux; amd64

```console
$ docker pull chronograf@sha256:e2c0fdc4b23b10f87ab9e5c9617d1d035619117fab9dc7159f5ac7431fdefef6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70589888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3363732a6c900845ecb011e33d91c62c5204787e64cac44ef62a20bca72f711a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:31:48 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:31:48 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:31:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:31:56 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:31:56 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:31:57 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:31:57 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:31:57 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:31:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:31:57 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c975e472544cfef3b1edb65cbba179cddff2a74f36ae6256e4c207282315d63`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 4.4 MB (4416570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87c10bc705875c556e87ee3caa63c1aa6c63043d84e145a0c757f4afd6d574a8`  
		Last Modified: Mon, 20 Mar 2023 23:33:35 GMT  
		Size: 34.7 MB (34737512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ebda569ad94c5137c57fafa4e571228c87b3cec5d0dd44169bc7add5ad7e8d0`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 12.3 KB (12252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:807dd9bb835ad8734aa84d019b96f2587d54ac55219cf08664b3b15c3b6de6e2`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ed53773262e6cc5a3a1e85d72db687fbcd6305f0f288c81927f1aab51961cfa`  
		Last Modified: Mon, 20 Mar 2023 23:33:31 GMT  
		Size: 239.0 B  
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
$ docker pull chronograf@sha256:3fc023fc5ab29b474f349b7f0442179a4dd1655af686fddffb26427125d85197
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67742600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc7d2cc708a431e1376870d18cbbf655ef11b1fe31a7ed2a31abb4d58bc7e6f`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:25 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:39:26 GMT
ENV CHRONOGRAF_VERSION=1.7.17
# Mon, 20 Mar 2023 23:39:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:39:33 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:39:33 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:39:33 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:39:34 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:39:34 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:39:34 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:39:34 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4ce4cbf4c5b42ca7aa605b687581c08ee9d305bec441f2d66bae7e12c74e66d`  
		Last Modified: Mon, 20 Mar 2023 23:40:28 GMT  
		Size: 4.4 MB (4418049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f9d9259d6017680ecb29212efc19f0b6f032c3ab955cb055992407e4bfbd3a2`  
		Last Modified: Mon, 20 Mar 2023 23:40:31 GMT  
		Size: 33.2 MB (33237338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a671a717b998aea3a2e768f65c029688aa5ec5c08d2614c1d15acb09015b921`  
		Last Modified: Mon, 20 Mar 2023 23:40:27 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746a063ad5ee911421b2327bb41984d6caed6d0627902bcc3fc5134051b4f47d`  
		Last Modified: Mon, 20 Mar 2023 23:40:27 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83093168381990146209da7573d0c3320f0479aced5bac134ced76b6a17d47c4`  
		Last Modified: Mon, 20 Mar 2023 23:40:27 GMT  
		Size: 240.0 B  
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
$ docker pull chronograf@sha256:bd8387a0b262a6d02e44dae0da2d3cb66f5ac6419eb74f8dd0a6d0539fbeddd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8` - linux; amd64

```console
$ docker pull chronograf@sha256:6d8aab472048af9fcfe63f2426b6d6074f82b2624dad147568e4794c2a526a2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71240985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a8800727ca7f82235d85c86fa8c4215c92436b3282545464fb08baf9395216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:32:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:32:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:32:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:32:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:25 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:25 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fbae0f9b7314139fc8cf586a274e59efd4bab289f8c70f51de567fd49e2c4`  
		Last Modified: Mon, 20 Mar 2023 23:33:56 GMT  
		Size: 5.2 MB (5226242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acec77e6552a9280c666981e321e653b5886b893ea0e28946bca1455dfe082e1`  
		Last Modified: Mon, 20 Mar 2023 23:34:00 GMT  
		Size: 34.6 MB (34578940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd11890012a801982d45eb1430d18638174989b75535cd023f8ed35422e529`  
		Last Modified: Mon, 20 Mar 2023 23:33:55 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc118a996cb046103c6d6e322fca9162b5674f28be36a42e4f4e7ad0057b3c78`  
		Last Modified: Mon, 20 Mar 2023 23:33:55 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89604b25ef1198ad5a8b24b75fd9157aeefb7e7c6aba46b581370cf53bf578f`  
		Last Modified: Mon, 20 Mar 2023 23:33:55 GMT  
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
$ docker pull chronograf@sha256:d51de7cd3682d7ba969740bfe50d6097a1d1d80144aabcd13608ce22d3e0c32c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee063d8791c8e623e46329f9798422f257b300d31161b665cf2dceeab46a9f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:39:43 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:39:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:39:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:39:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:39:54 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:39:54 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:39:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:39:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:39:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ac30e8757d0417421968a74cf9d8352c11cef6e9a94f8086b189076f4bb999`  
		Last Modified: Mon, 20 Mar 2023 23:40:40 GMT  
		Size: 5.2 MB (5209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11a7f8d85285be44ade601fab5d80158ebfd9a5d899372ee59116e106326a99`  
		Last Modified: Mon, 20 Mar 2023 23:40:42 GMT  
		Size: 32.6 MB (32643742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d738e1f44cf7440609dcc850a299a56370adf5a32ef69b4dc1dd114864c0d988`  
		Last Modified: Mon, 20 Mar 2023 23:40:39 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735ff42d98b63ceaa1ef4457d43e1c67c425b3d9d242fbda09c40919da302716`  
		Last Modified: Mon, 20 Mar 2023 23:40:39 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0b0c844fa408f19f3ab2796057a7fc9cb05a03fbe2f4ce3ffdee624f64dd19`  
		Last Modified: Mon, 20 Mar 2023 23:40:39 GMT  
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
$ docker pull chronograf@sha256:bd8387a0b262a6d02e44dae0da2d3cb66f5ac6419eb74f8dd0a6d0539fbeddd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.8.10` - linux; amd64

```console
$ docker pull chronograf@sha256:6d8aab472048af9fcfe63f2426b6d6074f82b2624dad147568e4794c2a526a2d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.2 MB (71240985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1a8800727ca7f82235d85c86fa8c4215c92436b3282545464fb08baf9395216`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:32:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:32:18 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:32:25 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:32:25 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:25 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:25 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:25 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:25 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:26 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:26 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fbae0f9b7314139fc8cf586a274e59efd4bab289f8c70f51de567fd49e2c4`  
		Last Modified: Mon, 20 Mar 2023 23:33:56 GMT  
		Size: 5.2 MB (5226242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acec77e6552a9280c666981e321e653b5886b893ea0e28946bca1455dfe082e1`  
		Last Modified: Mon, 20 Mar 2023 23:34:00 GMT  
		Size: 34.6 MB (34578940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd11890012a801982d45eb1430d18638174989b75535cd023f8ed35422e529`  
		Last Modified: Mon, 20 Mar 2023 23:33:55 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc118a996cb046103c6d6e322fca9162b5674f28be36a42e4f4e7ad0057b3c78`  
		Last Modified: Mon, 20 Mar 2023 23:33:55 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89604b25ef1198ad5a8b24b75fd9157aeefb7e7c6aba46b581370cf53bf578f`  
		Last Modified: Mon, 20 Mar 2023 23:33:55 GMT  
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
$ docker pull chronograf@sha256:d51de7cd3682d7ba969740bfe50d6097a1d1d80144aabcd13608ce22d3e0c32c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67940194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ee063d8791c8e623e46329f9798422f257b300d31161b665cf2dceeab46a9f4`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:39:43 GMT
ENV CHRONOGRAF_VERSION=1.8.10
# Mon, 20 Mar 2023 23:39:53 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:39:53 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:39:53 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:39:54 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:39:54 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:39:54 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:39:54 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:39:54 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ac30e8757d0417421968a74cf9d8352c11cef6e9a94f8086b189076f4bb999`  
		Last Modified: Mon, 20 Mar 2023 23:40:40 GMT  
		Size: 5.2 MB (5209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f11a7f8d85285be44ade601fab5d80158ebfd9a5d899372ee59116e106326a99`  
		Last Modified: Mon, 20 Mar 2023 23:40:42 GMT  
		Size: 32.6 MB (32643742 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d738e1f44cf7440609dcc850a299a56370adf5a32ef69b4dc1dd114864c0d988`  
		Last Modified: Mon, 20 Mar 2023 23:40:39 GMT  
		Size: 12.2 KB (12248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:735ff42d98b63ceaa1ef4457d43e1c67c425b3d9d242fbda09c40919da302716`  
		Last Modified: Mon, 20 Mar 2023 23:40:39 GMT  
		Size: 11.9 KB (11907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0b0c844fa408f19f3ab2796057a7fc9cb05a03fbe2f4ce3ffdee624f64dd19`  
		Last Modified: Mon, 20 Mar 2023 23:40:39 GMT  
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
$ docker pull chronograf@sha256:d117a63bd047ce7b99dd4cc88ce0d19f5ee18e4a8f6a367e651aeb880f4f887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9` - linux; amd64

```console
$ docker pull chronograf@sha256:a29949fe7f1e0a34cdd574a3fc441ae8b3ab002ed2d40ce278c86c14feb348e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71888592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ff963110e4783d489f6e57b8d2e0ef19d678606c8065fad2c687d9960209a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:32:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:32:36 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:32:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:32:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:42 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:42 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fbae0f9b7314139fc8cf586a274e59efd4bab289f8c70f51de567fd49e2c4`  
		Last Modified: Mon, 20 Mar 2023 23:33:56 GMT  
		Size: 5.2 MB (5226242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e64632d10c7d251f06d42623582aea7f99f66cde82800e71cc0101afdc70595`  
		Last Modified: Mon, 20 Mar 2023 23:34:23 GMT  
		Size: 35.2 MB (35226549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaff3af0e89eda87f6f60dae8a97c7763f39ab641f3c0d56dd9574759b1021d`  
		Last Modified: Mon, 20 Mar 2023 23:34:19 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7583cb3402b9212c0ea4f4bd188316136f03c012ff75be48cd24b40dd2140bd1`  
		Last Modified: Mon, 20 Mar 2023 23:34:19 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb7f8d0554b3ef4075da18017369f5db949b8e2638ecd328cab4c1168710b4`  
		Last Modified: Mon, 20 Mar 2023 23:34:19 GMT  
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
$ docker pull chronograf@sha256:435a3e1b42647bd15265d77a3c8a01900c09a1fba764b78f957296c415caf956
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68691874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1ee863858d09008ceadf05d7cbf78e1c0211b0890e2ce1cfdfd7d0ee00d275`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:39:57 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:40:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:40:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:40:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:40:03 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:40:03 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:40:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:40:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:40:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ac30e8757d0417421968a74cf9d8352c11cef6e9a94f8086b189076f4bb999`  
		Last Modified: Mon, 20 Mar 2023 23:40:40 GMT  
		Size: 5.2 MB (5209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c0857135d7131cb5b964095db26c3cee9e62f1e0d822fa6e77979bcc41efa`  
		Last Modified: Mon, 20 Mar 2023 23:40:53 GMT  
		Size: 33.4 MB (33395417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d23fd3bdce2eae590365a8e7aab49d3bb2a54a5a6ba5e1258da49df39d5b7e7`  
		Last Modified: Mon, 20 Mar 2023 23:40:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6c2c633d41729429102059ba556366c6dd29b502c6d4635b89c75f0d894335`  
		Last Modified: Mon, 20 Mar 2023 23:40:50 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21347078584914d161baf40a398bec399a1b4373fff84dfa8889d119db421ead`  
		Last Modified: Mon, 20 Mar 2023 23:40:50 GMT  
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
$ docker pull chronograf@sha256:d117a63bd047ce7b99dd4cc88ce0d19f5ee18e4a8f6a367e651aeb880f4f887d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:1.9.4` - linux; amd64

```console
$ docker pull chronograf@sha256:a29949fe7f1e0a34cdd574a3fc441ae8b3ab002ed2d40ce278c86c14feb348e9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71888592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ff963110e4783d489f6e57b8d2e0ef19d678606c8065fad2c687d9960209a9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:32:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:32:36 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:32:41 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:32:42 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:42 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:42 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:42 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:32:42 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:32:42 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:32:42 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fbae0f9b7314139fc8cf586a274e59efd4bab289f8c70f51de567fd49e2c4`  
		Last Modified: Mon, 20 Mar 2023 23:33:56 GMT  
		Size: 5.2 MB (5226242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e64632d10c7d251f06d42623582aea7f99f66cde82800e71cc0101afdc70595`  
		Last Modified: Mon, 20 Mar 2023 23:34:23 GMT  
		Size: 35.2 MB (35226549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecaff3af0e89eda87f6f60dae8a97c7763f39ab641f3c0d56dd9574759b1021d`  
		Last Modified: Mon, 20 Mar 2023 23:34:19 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7583cb3402b9212c0ea4f4bd188316136f03c012ff75be48cd24b40dd2140bd1`  
		Last Modified: Mon, 20 Mar 2023 23:34:19 GMT  
		Size: 11.9 KB (11909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45eb7f8d0554b3ef4075da18017369f5db949b8e2638ecd328cab4c1168710b4`  
		Last Modified: Mon, 20 Mar 2023 23:34:19 GMT  
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
$ docker pull chronograf@sha256:435a3e1b42647bd15265d77a3c8a01900c09a1fba764b78f957296c415caf956
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68691874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1ee863858d09008ceadf05d7cbf78e1c0211b0890e2ce1cfdfd7d0ee00d275`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:39:57 GMT
ENV CHRONOGRAF_VERSION=1.9.4
# Mon, 20 Mar 2023 23:40:03 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:40:03 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:40:03 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:40:03 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:40:03 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:40:03 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:40:03 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:40:03 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ac30e8757d0417421968a74cf9d8352c11cef6e9a94f8086b189076f4bb999`  
		Last Modified: Mon, 20 Mar 2023 23:40:40 GMT  
		Size: 5.2 MB (5209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b80c0857135d7131cb5b964095db26c3cee9e62f1e0d822fa6e77979bcc41efa`  
		Last Modified: Mon, 20 Mar 2023 23:40:53 GMT  
		Size: 33.4 MB (33395417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d23fd3bdce2eae590365a8e7aab49d3bb2a54a5a6ba5e1258da49df39d5b7e7`  
		Last Modified: Mon, 20 Mar 2023 23:40:50 GMT  
		Size: 12.2 KB (12250 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6c2c633d41729429102059ba556366c6dd29b502c6d4635b89c75f0d894335`  
		Last Modified: Mon, 20 Mar 2023 23:40:50 GMT  
		Size: 11.9 KB (11910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21347078584914d161baf40a398bec399a1b4373fff84dfa8889d119db421ead`  
		Last Modified: Mon, 20 Mar 2023 23:40:50 GMT  
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
$ docker pull chronograf@sha256:3e3e6978901d5091c39e2cd8438fac8767b1db617169e881c94ff9fe5ccb45e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `chronograf:latest` - linux; amd64

```console
$ docker pull chronograf@sha256:c0ab4053aba5da7bbe55c35abd5184117a0ee9146155b112404e3e2329f273a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82803459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e8332c725f9d526950f495821bee19fc234d603ad6102fa8ced1c9c6a6b95a`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:32:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:32:53 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:32:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:32:59 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:32:59 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:32:59 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:32:59 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:33:00 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:33:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:33:00 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99fbae0f9b7314139fc8cf586a274e59efd4bab289f8c70f51de567fd49e2c4`  
		Last Modified: Mon, 20 Mar 2023 23:33:56 GMT  
		Size: 5.2 MB (5226242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337a768d84760225d90be0f3e833e89225e0387799cdc04019a8a7a0bc54e99a`  
		Last Modified: Mon, 20 Mar 2023 23:34:49 GMT  
		Size: 46.1 MB (46141408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959c874c2f7f1c46b96b10658e6ae9a641c1296501ef204cb5ddafa29033bb22`  
		Last Modified: Mon, 20 Mar 2023 23:34:43 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a62ea9549eea35393a5f46ef374c9787a4eecf9c5b85ba384c92f545cac0ba76`  
		Last Modified: Mon, 20 Mar 2023 23:34:43 GMT  
		Size: 11.9 KB (11913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6263d6fa9c8c2ce72bb2b95f624fbf746bbdb6b68cfe2c1bb14087911d63fb85`  
		Last Modified: Mon, 20 Mar 2023 23:34:44 GMT  
		Size: 240.0 B  
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
$ docker pull chronograf@sha256:d1306cd7d2003990a8228c85cc092841f4c1569e432c76546f82fef363581d01
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79151143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6937b7c88a5861070c99f0d7f9fa747da4503cc1b3634ca849625ab5b59da555`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["chronograf"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Mon, 20 Mar 2023 23:39:43 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apt-get update && apt-get install -y gnupg ca-certificates dirmngr --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Mon, 20 Mar 2023 23:40:06 GMT
ENV CHRONOGRAF_VERSION=1.10.1
# Mon, 20 Mar 2023 23:40:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     set -x &&     apt-get update && apt-get install -y ca-certificates curl --no-install-recommends &&     rm -rf /var/lib/apt/lists/* &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc" &&     curl -SLO "https://dl.influxdata.com/chronograf/releases/chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb" &&     gpg --batch --verify chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb.asc chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     dpkg -i chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb &&     rm -f chronograf_${CHRONOGRAF_VERSION}_${ARCH}.deb* &&     apt-get purge -y --auto-remove $buildDeps
# Mon, 20 Mar 2023 23:40:13 GMT
COPY file:6403df1bf15a98453f66ca6b38ee538c184409065ea1d3c321788dec9eaa5c77 in /usr/share/chronograf/LICENSE 
# Mon, 20 Mar 2023 23:40:13 GMT
COPY file:6a5854b87d89e3055231dd56f8f199c325f44eeed8faed4cf32833126a5b9cd9 in /usr/share/chronograf/agpl-3.0.md 
# Mon, 20 Mar 2023 23:40:14 GMT
EXPOSE 8888
# Mon, 20 Mar 2023 23:40:14 GMT
VOLUME [/var/lib/chronograf]
# Mon, 20 Mar 2023 23:40:14 GMT
COPY file:7ce45912f7e80a04754c20ff31c757dd5de5eb9a5845af3b183b4a5227dd1c1e in /entrypoint.sh 
# Mon, 20 Mar 2023 23:40:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Mon, 20 Mar 2023 23:40:14 GMT
CMD ["chronograf"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41ac30e8757d0417421968a74cf9d8352c11cef6e9a94f8086b189076f4bb999`  
		Last Modified: Mon, 20 Mar 2023 23:40:40 GMT  
		Size: 5.2 MB (5209244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1822cac3aa5821565094fbcf277937f8fba866c6702ad0fa77fc2f46f7a925d3`  
		Last Modified: Mon, 20 Mar 2023 23:41:06 GMT  
		Size: 43.9 MB (43854681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73d030f0702d70868441768ad3edcdec05d93cd10056556f129b5c2785407d79`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
		Size: 12.3 KB (12253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94b39f86ccdb7ca8aade7d10e09ee8718dfe19693fa53e3d4c1721404dd4b2b9`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
		Size: 11.9 KB (11912 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfdb045b7a48f0a73099313d3eee8c52df4dd478d79907253f6bd796d3906222`  
		Last Modified: Mon, 20 Mar 2023 23:41:02 GMT  
		Size: 239.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
