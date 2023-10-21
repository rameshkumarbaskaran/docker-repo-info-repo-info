<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `telegraf`

-	[`telegraf:1.26`](#telegraf126)
-	[`telegraf:1.26-alpine`](#telegraf126-alpine)
-	[`telegraf:1.26.3`](#telegraf1263)
-	[`telegraf:1.26.3-alpine`](#telegraf1263-alpine)
-	[`telegraf:1.27`](#telegraf127)
-	[`telegraf:1.27-alpine`](#telegraf127-alpine)
-	[`telegraf:1.27.4`](#telegraf1274)
-	[`telegraf:1.27.4-alpine`](#telegraf1274-alpine)
-	[`telegraf:1.28`](#telegraf128)
-	[`telegraf:1.28-alpine`](#telegraf128-alpine)
-	[`telegraf:1.28.2`](#telegraf1282)
-	[`telegraf:1.28.2-alpine`](#telegraf1282-alpine)
-	[`telegraf:alpine`](#telegrafalpine)
-	[`telegraf:latest`](#telegraflatest)

## `telegraf:1.26`

```console
$ docker pull telegraf@sha256:d5dfeb9ad075652027277ebb1e254e8a2f34bb3e516597e4b404cb51796a612f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.26` - linux; amd64

```console
$ docker pull telegraf@sha256:bbb3e0fbe5485b7520eda6a69b5b0693b823f8bb6f00ffc66993971e5f6fd76e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140137296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de14ce7b951f96decc6b0c69575124f5a8fe089e6f6d38f268d6254a9360cbd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 11:11:18 GMT
ENV TELEGRAF_VERSION=1.26.3
# Thu, 12 Oct 2023 11:11:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 11:11:23 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 11:11:23 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 11:11:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 11:11:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dedceb9c21c46986231d9dfb896b37cfc470d67799e7e919a641ac54dcc9eed`  
		Last Modified: Thu, 12 Oct 2023 03:29:53 GMT  
		Size: 15.8 MB (15764226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b56c60dbc6689312093d86d865bfb5faaf91a6b6e092e49a86a3f1601534595`  
		Last Modified: Thu, 12 Oct 2023 11:12:19 GMT  
		Size: 18.8 MB (18760360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0bdc028c242a5eaeb3b41d5f2171b958786df7c2b451c6cc74e8c3a629b2d`  
		Last Modified: Thu, 12 Oct 2023 11:12:16 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897933267ac7ebb290278c8771c61974d3e58adef54510e106004aa798f656b8`  
		Last Modified: Thu, 12 Oct 2023 11:12:23 GMT  
		Size: 50.6 MB (50552525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f4ce388f50d8238730db71d67bd6a1e82c17a70c343a0ecd9e990afae2c913`  
		Last Modified: Thu, 12 Oct 2023 11:12:16 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7bed3b8b0a12578caad50525dd6b68db670e004067328812582761f2a0006696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129843357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8debfb982c95dc5c49e00e812d4b828ce093c99802cac0fee6f8e4ef31ba1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:19 GMT
ADD file:684f3634c6b747a4caad8f9f820cc02b53a2122591fe215935c5497ec234c3ad in / 
# Wed, 11 Oct 2023 17:42:20 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:47:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 18:09:05 GMT
ENV TELEGRAF_VERSION=1.26.3
# Thu, 12 Oct 2023 18:09:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 18:09:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 18:09:14 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 18:09:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 18:09:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:33d0c7672db93e653471872c639cd6129ec25c168942e15a008c4920cafe62d7`  
		Last Modified: Wed, 11 Oct 2023 17:46:42 GMT  
		Size: 50.2 MB (50215704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe33e05af9470f2356c8047560fded363dda4990bb2d70e9194f0dca496bb82`  
		Last Modified: Thu, 12 Oct 2023 03:57:11 GMT  
		Size: 14.9 MB (14879720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a7a0fd4695ef816fa3faf9f741e7314f175d3c29ebbfbb4d7b3f84cf248d0`  
		Last Modified: Thu, 12 Oct 2023 18:10:00 GMT  
		Size: 17.5 MB (17463091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1502db49d0ab72b24b402f2132f5d969468aedec133498fb917e4f4b01f156cc`  
		Last Modified: Thu, 12 Oct 2023 18:09:57 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5ff96bb235a30bf2cc32cad4f84de45d710ff5c0da876c2a9279f92709d3dd`  
		Last Modified: Thu, 12 Oct 2023 18:10:05 GMT  
		Size: 47.3 MB (47282686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecef69aa20f9d0347ffcbd157a601483673b358d46b57e853b693f45e23b378`  
		Last Modified: Thu, 12 Oct 2023 18:09:57 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4fec51da2fee2da8fd5a0130c32ebb35e3e3c2562863875ab0604df5e3b290e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134031211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e88bac8e1a45ae7484659ee796eb15942d916856c7c4d5531ca91a45d99d9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 14:29:32 GMT
ENV TELEGRAF_VERSION=1.26.3
# Thu, 12 Oct 2023 14:29:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 14:29:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 14:29:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 14:29:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 14:29:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7a630df11a812111dd2b7f5b819a692f2350ad055fab0cd3e60b322c2eead5`  
		Last Modified: Wed, 11 Oct 2023 19:54:57 GMT  
		Size: 15.7 MB (15749899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682476726f98f1b47bdcc09af487f661bba163c95bd353bbe4a52515a9a1ce43`  
		Last Modified: Thu, 12 Oct 2023 14:30:31 GMT  
		Size: 18.6 MB (18599450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba91a0d171999e89d299ab23183d1ea404135a1f0f53ea40ceef4a0c5bd38a`  
		Last Modified: Thu, 12 Oct 2023 14:30:29 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710e64a1595e2742cf57f63fc8f9d67c1fd2bfc1d910375c31b7ebfd6610e8b4`  
		Last Modified: Thu, 12 Oct 2023 14:30:34 GMT  
		Size: 46.0 MB (45971894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dde7b24f8662b819c366bc7b2e8a5ceb286311a553c3fa491c4f5859725737`  
		Last Modified: Thu, 12 Oct 2023 14:30:29 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.26-alpine`

```console
$ docker pull telegraf@sha256:2fb0d7dcc11ab727d9e2e5b05c0ac82be740a22936117d76b9914f7a8df0959f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.26-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd6fdb97c35d23921c56ac02294bc74222cf7edb96064fa1b314f8e2fc630126
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56442971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65b8f7eed3acc3df20dedbd2c4de09c5a7b614822afa9fabe928ee01bf7f99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:36 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:41:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:41:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:41:43 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:41:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:41:44 GMT
CMD ["telegraf"]
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
	-	`sha256:5ce697a40ba666c0b939bdfff27ea7f13e38a2363f3ea3aacfd8d5d5aa7239a5`  
		Last Modified: Sat, 21 Oct 2023 03:42:33 GMT  
		Size: 2.7 MB (2671799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb68957bb0474b77a292c6f1875391f2fde9feeee846b9585aaf1b1784e905`  
		Last Modified: Sat, 21 Oct 2023 03:42:40 GMT  
		Size: 50.4 MB (50391960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42df3bbacb302690503e1ab44cdae6eec964b9467d9d8d98f0c965cec1b102`  
		Last Modified: Sat, 21 Oct 2023 03:42:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:886ff7d38f0f58e105588b7098329984ef8e1d3c543649415c2150710676d31a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51775137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c79d58dc20ceb6d3890cb65eb511e3e18e20510aa6c2193ed12affd33b3ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 03:05:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:05 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:05:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:16 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20cffce9f02c4faf5b734eac9c68df5443330a55a792e82a17d54196a5def44`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b550fd38b5dfc7dab42f13c3a28e8c9d6e08aaf414321bbf9b926e8bc47b3`  
		Last Modified: Sat, 21 Oct 2023 03:06:05 GMT  
		Size: 2.7 MB (2703935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aaa5e94e88830c33ad85ebe381728f95c9fba46a2f0b587a85ae055ac3ce7d`  
		Last Modified: Sat, 21 Oct 2023 03:06:09 GMT  
		Size: 45.8 MB (45812303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afdf42e99e6b76dcfc17aaacc7e3506486b18e712855245382746a6f298ba07`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.26.3`

```console
$ docker pull telegraf@sha256:d5dfeb9ad075652027277ebb1e254e8a2f34bb3e516597e4b404cb51796a612f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.26.3` - linux; amd64

```console
$ docker pull telegraf@sha256:bbb3e0fbe5485b7520eda6a69b5b0693b823f8bb6f00ffc66993971e5f6fd76e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.1 MB (140137296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de14ce7b951f96decc6b0c69575124f5a8fe089e6f6d38f268d6254a9360cbd7`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:35:01 GMT
ADD file:8a9222387b89a9ac763fd72610ce01ab17f64387cbfde30a6af1861a82030aad in / 
# Wed, 11 Oct 2023 18:35:01 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:17 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:18 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 11:11:18 GMT
ENV TELEGRAF_VERSION=1.26.3
# Thu, 12 Oct 2023 11:11:23 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 11:11:23 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 11:11:23 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 11:11:23 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 11:11:23 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:69b3efbf67c2d9a46fdfdc8480b5a03ef73e9999a53aad57213447784f01eb6e`  
		Last Modified: Wed, 11 Oct 2023 18:39:54 GMT  
		Size: 55.1 MB (55058028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dedceb9c21c46986231d9dfb896b37cfc470d67799e7e919a641ac54dcc9eed`  
		Last Modified: Thu, 12 Oct 2023 03:29:53 GMT  
		Size: 15.8 MB (15764226 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b56c60dbc6689312093d86d865bfb5faaf91a6b6e092e49a86a3f1601534595`  
		Last Modified: Thu, 12 Oct 2023 11:12:19 GMT  
		Size: 18.8 MB (18760360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5b0bdc028c242a5eaeb3b41d5f2171b958786df7c2b451c6cc74e8c3a629b2d`  
		Last Modified: Thu, 12 Oct 2023 11:12:16 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:897933267ac7ebb290278c8771c61974d3e58adef54510e106004aa798f656b8`  
		Last Modified: Thu, 12 Oct 2023 11:12:23 GMT  
		Size: 50.6 MB (50552525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f4ce388f50d8238730db71d67bd6a1e82c17a70c343a0ecd9e990afae2c913`  
		Last Modified: Thu, 12 Oct 2023 11:12:16 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26.3` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:7bed3b8b0a12578caad50525dd6b68db670e004067328812582761f2a0006696
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.8 MB (129843357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb8debfb982c95dc5c49e00e812d4b828ce093c99802cac0fee6f8e4ef31ba1`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 17:42:19 GMT
ADD file:684f3634c6b747a4caad8f9f820cc02b53a2122591fe215935c5497ec234c3ad in / 
# Wed, 11 Oct 2023 17:42:20 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:47:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:03 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:05 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 18:09:05 GMT
ENV TELEGRAF_VERSION=1.26.3
# Thu, 12 Oct 2023 18:09:13 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 18:09:14 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 18:09:14 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 18:09:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 18:09:14 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:33d0c7672db93e653471872c639cd6129ec25c168942e15a008c4920cafe62d7`  
		Last Modified: Wed, 11 Oct 2023 17:46:42 GMT  
		Size: 50.2 MB (50215704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe33e05af9470f2356c8047560fded363dda4990bb2d70e9194f0dca496bb82`  
		Last Modified: Thu, 12 Oct 2023 03:57:11 GMT  
		Size: 14.9 MB (14879720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec9a7a0fd4695ef816fa3faf9f741e7314f175d3c29ebbfbb4d7b3f84cf248d0`  
		Last Modified: Thu, 12 Oct 2023 18:10:00 GMT  
		Size: 17.5 MB (17463091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1502db49d0ab72b24b402f2132f5d969468aedec133498fb917e4f4b01f156cc`  
		Last Modified: Thu, 12 Oct 2023 18:09:57 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb5ff96bb235a30bf2cc32cad4f84de45d710ff5c0da876c2a9279f92709d3dd`  
		Last Modified: Thu, 12 Oct 2023 18:10:05 GMT  
		Size: 47.3 MB (47282686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ecef69aa20f9d0347ffcbd157a601483673b358d46b57e853b693f45e23b378`  
		Last Modified: Thu, 12 Oct 2023 18:09:57 GMT  
		Size: 344.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26.3` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:4fec51da2fee2da8fd5a0130c32ebb35e3e3c2562863875ab0604df5e3b290e0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.0 MB (134031211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e88bac8e1a45ae7484659ee796eb15942d916856c7c4d5531ca91a45d99d9d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:46:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:31 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:32 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 14:29:32 GMT
ENV TELEGRAF_VERSION=1.26.3
# Thu, 12 Oct 2023 14:29:38 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 14:29:39 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 14:29:39 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 14:29:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 14:29:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd7a630df11a812111dd2b7f5b819a692f2350ad055fab0cd3e60b322c2eead5`  
		Last Modified: Wed, 11 Oct 2023 19:54:57 GMT  
		Size: 15.7 MB (15749899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682476726f98f1b47bdcc09af487f661bba163c95bd353bbe4a52515a9a1ce43`  
		Last Modified: Thu, 12 Oct 2023 14:30:31 GMT  
		Size: 18.6 MB (18599450 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cba91a0d171999e89d299ab23183d1ea404135a1f0f53ea40ceef4a0c5bd38a`  
		Last Modified: Thu, 12 Oct 2023 14:30:29 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:710e64a1595e2742cf57f63fc8f9d67c1fd2bfc1d910375c31b7ebfd6610e8b4`  
		Last Modified: Thu, 12 Oct 2023 14:30:34 GMT  
		Size: 46.0 MB (45971894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2dde7b24f8662b819c366bc7b2e8a5ceb286311a553c3fa491c4f5859725737`  
		Last Modified: Thu, 12 Oct 2023 14:30:29 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.26.3-alpine`

```console
$ docker pull telegraf@sha256:2fb0d7dcc11ab727d9e2e5b05c0ac82be740a22936117d76b9914f7a8df0959f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.26.3-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:cd6fdb97c35d23921c56ac02294bc74222cf7edb96064fa1b314f8e2fc630126
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56442971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd65b8f7eed3acc3df20dedbd2c4de09c5a7b614822afa9fabe928ee01bf7f99`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:26 GMT
ADD file:6dd87346b8be240b21b4f4d9296253bf0d28b6579aa52d2118872e3936963b6b in / 
# Mon, 07 Aug 2023 19:20:26 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:29:21 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:36 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:36 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:41:43 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:41:43 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:41:43 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:41:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:41:44 GMT
CMD ["telegraf"]
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
	-	`sha256:5ce697a40ba666c0b939bdfff27ea7f13e38a2363f3ea3aacfd8d5d5aa7239a5`  
		Last Modified: Sat, 21 Oct 2023 03:42:33 GMT  
		Size: 2.7 MB (2671799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbb68957bb0474b77a292c6f1875391f2fde9feeee846b9585aaf1b1784e905`  
		Last Modified: Sat, 21 Oct 2023 03:42:40 GMT  
		Size: 50.4 MB (50391960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb42df3bbacb302690503e1ab44cdae6eec964b9467d9d8d98f0c965cec1b102`  
		Last Modified: Sat, 21 Oct 2023 03:42:32 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.26.3-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:886ff7d38f0f58e105588b7098329984ef8e1d3c543649415c2150710676d31a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51775137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98c79d58dc20ceb6d3890cb65eb511e3e18e20510aa6c2193ed12affd33b3ca3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:22 GMT
ADD file:9e054a25c83111adc857a7f988336ee40eea5e1794ed30a80d465e8d472342e2 in / 
# Mon, 07 Aug 2023 19:39:22 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 03:05:03 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:05 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:05 GMT
ENV TELEGRAF_VERSION=1.26.3
# Sat, 21 Oct 2023 03:05:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:16 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:16 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:16 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:4060ece20d7ac783f52cbe28a35fd5b06f90f7b4d773bae0d956024e85ff35b6`  
		Last Modified: Mon, 07 Aug 2023 19:39:59 GMT  
		Size: 3.3 MB (3258290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d20cffce9f02c4faf5b734eac9c68df5443330a55a792e82a17d54196a5def44`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 281.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:995b550fd38b5dfc7dab42f13c3a28e8c9d6e08aaf414321bbf9b926e8bc47b3`  
		Last Modified: Sat, 21 Oct 2023 03:06:05 GMT  
		Size: 2.7 MB (2703935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6aaa5e94e88830c33ad85ebe381728f95c9fba46a2f0b587a85ae055ac3ce7d`  
		Last Modified: Sat, 21 Oct 2023 03:06:09 GMT  
		Size: 45.8 MB (45812303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afdf42e99e6b76dcfc17aaacc7e3506486b18e712855245382746a6f298ba07`  
		Last Modified: Sat, 21 Oct 2023 03:06:04 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27`

```console
$ docker pull telegraf@sha256:a328b76b0901d8e0e02b1bc481cc3d5e3e74bd63366736ea99811a83e706e530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27` - linux; amd64

```console
$ docker pull telegraf@sha256:1a885bfd4ae81b04b3f2506b791033a065cdffc829ab145042f23cecbbcc10dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148107921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd24cf32ac5228a36bb2f3fea57cd5261be6e34635344b0fd303dc011ec64133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:19:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 11:11:38 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 12 Oct 2023 11:11:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 11:11:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 11:11:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 11:11:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 11:11:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc26d841b4acc2562483bf393ce1cf8bc358ced09ccd825425226827c79c92`  
		Last Modified: Thu, 12 Oct 2023 03:28:45 GMT  
		Size: 24.1 MB (24051259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42938defa8a6b527ab4fb0f8be74ac2b7c945f5518627ce9e869533ce2c3050`  
		Last Modified: Thu, 12 Oct 2023 11:12:37 GMT  
		Size: 19.1 MB (19145561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366994b97c2f17c0fe06554587854beea020e47b89b927da0bd69563cf6e7495`  
		Last Modified: Thu, 12 Oct 2023 11:12:33 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1dc711788267bfa36638f99de0f0b2ee16ef1821aa788820621f2de21c6e14`  
		Last Modified: Thu, 12 Oct 2023 11:12:42 GMT  
		Size: 55.3 MB (55326720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd521a0eade35ec1e22a15308391ac6bdb3c6e2ebf35cfeabd6317c47cdf983f`  
		Last Modified: Thu, 12 Oct 2023 11:12:33 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ba6e80611da7c069c3bb3c3fcdba42345839aaa17b693c7a83930bda322e0b92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883a3dd42107e599d2bfd0a7e96ee73a467358c7089da74ac876c0550543c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:59 GMT
ADD file:914e8a43f38c44fe9a6aabf05bbf3ebad5530966a354c8e7bb873c0842d35256 in / 
# Wed, 11 Oct 2023 17:42:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:45:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 18:09:27 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 12 Oct 2023 18:09:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 18:09:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 18:09:37 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 18:09:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 18:09:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:65b9f3344eccdad2292cc7eec885befe05a52ec1136e145130c849441428eee6`  
		Last Modified: Wed, 11 Oct 2023 17:45:56 GMT  
		Size: 45.2 MB (45180287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbdddb82776e8c5901a821d5034c82b0fcba2993014440cd080d0592cd49616`  
		Last Modified: Thu, 12 Oct 2023 03:55:58 GMT  
		Size: 22.0 MB (21953833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fd75bac7be32a4c2229f7c55dc64abed60b0a8cb9e2fdd864034a57600f2fa`  
		Last Modified: Thu, 12 Oct 2023 18:10:18 GMT  
		Size: 18.0 MB (17991786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c42367e4c938159668542b19b5ed09bc2b4b58ea053c02eebd94a8f50a3210`  
		Last Modified: Thu, 12 Oct 2023 18:10:15 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2f6ab051da012976b25f16ff885710a712d504e1106aa76ea5fbfc6e76a1ba`  
		Last Modified: Thu, 12 Oct 2023 18:10:23 GMT  
		Size: 51.5 MB (51505765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe62f49d1392d913c5b968aa8b2eb3707b47a864e3ef51b58cd375244250b389`  
		Last Modified: Thu, 12 Oct 2023 18:10:15 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:37fc84c2b57e5add5ce617509395b946a9b20ba40fb7f61b651eda0c7e04ff4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142240989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fb450de10f83ccf92f2ece4179fcb11bbbb7c099942b09ec841fa4c2cae071`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:44:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 14:29:53 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 12 Oct 2023 14:29:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 14:30:00 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 14:30:00 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 14:30:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 14:30:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7541d83e7b8c0f5f6cacacddfcf5fdd942793f13418bc4645203b4ab4f3de3`  
		Last Modified: Wed, 11 Oct 2023 19:53:48 GMT  
		Size: 23.6 MB (23588086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b6c2ba718a2e4c688d25c56a5ccd994c3d661135cec510532624c88d9120a0`  
		Last Modified: Thu, 12 Oct 2023 14:30:45 GMT  
		Size: 19.1 MB (19079557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df642945c62c789f355dc49ee06e4cf84cf254d0700d6ca01f983950a226a70`  
		Last Modified: Thu, 12 Oct 2023 14:30:43 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb876c2e72f426105b4e693c8d85f6abbd7a16d9b32fd024f966853fc8353a`  
		Last Modified: Thu, 12 Oct 2023 14:30:50 GMT  
		Size: 50.0 MB (49958610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4396b0321f3b9b0da919f9248cf5d9ba9a3795bad0d0dd1b0916b4f269ed3ea4`  
		Last Modified: Thu, 12 Oct 2023 14:30:43 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27-alpine`

```console
$ docker pull telegraf@sha256:f77ed7dddb02a84b5bdd31d9f89a018ee08edea598b7da9dd81e5d66577f651b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.27-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6eccd860212b44034872f6130348edf970d72a900afcbafd229208de4d29b9d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61199653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48fd08420a9d1b3991e3781cda8fb3b5c38d0211c2fef5fef53881f9389ef80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:50 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:42:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:42:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:42:01 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:42:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:42:01 GMT
CMD ["telegraf"]
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
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450dcdf691f11f970afef73d942c63e6161a568b77622ff4107e6478725af37c`  
		Last Modified: Sat, 21 Oct 2023 03:42:59 GMT  
		Size: 55.2 MB (55152107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102b1a74ea9501518451d0ae11db2bee8fe1b66599de184e0ea725f93b37782e`  
		Last Modified: Sat, 21 Oct 2023 03:42:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b4e52a8cd5440d35e1009c242974397bdcc55a2a50066ed33ab4fddcc7e01b93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55801017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d412a0494e0a1ec188214fe6a98c9bad9ded0972205b6354751f16585a8e3f3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:22 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:05:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef6f17a9a0ea6e7a97c008cc018d7359892e7edc9648fa9028a0c8f9ca1174`  
		Last Modified: Sat, 21 Oct 2023 03:06:25 GMT  
		Size: 49.8 MB (49795386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab157c6d650bcef23423e9caf5874f8b88eab7ddf83f54c5acd6e656238c20a`  
		Last Modified: Sat, 21 Oct 2023 03:06:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4`

```console
$ docker pull telegraf@sha256:a328b76b0901d8e0e02b1bc481cc3d5e3e74bd63366736ea99811a83e706e530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.27.4` - linux; amd64

```console
$ docker pull telegraf@sha256:1a885bfd4ae81b04b3f2506b791033a065cdffc829ab145042f23cecbbcc10dd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148107921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd24cf32ac5228a36bb2f3fea57cd5261be6e34635344b0fd303dc011ec64133`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:19:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 11:11:38 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 12 Oct 2023 11:11:45 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 11:11:46 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 11:11:46 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 11:11:46 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 11:11:46 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc26d841b4acc2562483bf393ce1cf8bc358ced09ccd825425226827c79c92`  
		Last Modified: Thu, 12 Oct 2023 03:28:45 GMT  
		Size: 24.1 MB (24051259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42938defa8a6b527ab4fb0f8be74ac2b7c945f5518627ce9e869533ce2c3050`  
		Last Modified: Thu, 12 Oct 2023 11:12:37 GMT  
		Size: 19.1 MB (19145561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366994b97c2f17c0fe06554587854beea020e47b89b927da0bd69563cf6e7495`  
		Last Modified: Thu, 12 Oct 2023 11:12:33 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b1dc711788267bfa36638f99de0f0b2ee16ef1821aa788820621f2de21c6e14`  
		Last Modified: Thu, 12 Oct 2023 11:12:42 GMT  
		Size: 55.3 MB (55326720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd521a0eade35ec1e22a15308391ac6bdb3c6e2ebf35cfeabd6317c47cdf983f`  
		Last Modified: Thu, 12 Oct 2023 11:12:33 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:ba6e80611da7c069c3bb3c3fcdba42345839aaa17b693c7a83930bda322e0b92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.6 MB (136633828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5883a3dd42107e599d2bfd0a7e96ee73a467358c7089da74ac876c0550543c45`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:59 GMT
ADD file:914e8a43f38c44fe9a6aabf05bbf3ebad5530966a354c8e7bb873c0842d35256 in / 
# Wed, 11 Oct 2023 17:42:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:45:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 18:09:27 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 12 Oct 2023 18:09:36 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 18:09:37 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 18:09:37 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 18:09:37 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 18:09:37 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:65b9f3344eccdad2292cc7eec885befe05a52ec1136e145130c849441428eee6`  
		Last Modified: Wed, 11 Oct 2023 17:45:56 GMT  
		Size: 45.2 MB (45180287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbdddb82776e8c5901a821d5034c82b0fcba2993014440cd080d0592cd49616`  
		Last Modified: Thu, 12 Oct 2023 03:55:58 GMT  
		Size: 22.0 MB (21953833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fd75bac7be32a4c2229f7c55dc64abed60b0a8cb9e2fdd864034a57600f2fa`  
		Last Modified: Thu, 12 Oct 2023 18:10:18 GMT  
		Size: 18.0 MB (17991786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c42367e4c938159668542b19b5ed09bc2b4b58ea053c02eebd94a8f50a3210`  
		Last Modified: Thu, 12 Oct 2023 18:10:15 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b2f6ab051da012976b25f16ff885710a712d504e1106aa76ea5fbfc6e76a1ba`  
		Last Modified: Thu, 12 Oct 2023 18:10:23 GMT  
		Size: 51.5 MB (51505765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe62f49d1392d913c5b968aa8b2eb3707b47a864e3ef51b58cd375244250b389`  
		Last Modified: Thu, 12 Oct 2023 18:10:15 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:37fc84c2b57e5add5ce617509395b946a9b20ba40fb7f61b651eda0c7e04ff4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.2 MB (142240989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fb450de10f83ccf92f2ece4179fcb11bbbb7c099942b09ec841fa4c2cae071`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:44:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 14:29:53 GMT
ENV TELEGRAF_VERSION=1.27.4
# Thu, 12 Oct 2023 14:29:59 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 14:30:00 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 14:30:00 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 14:30:00 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 14:30:00 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7541d83e7b8c0f5f6cacacddfcf5fdd942793f13418bc4645203b4ab4f3de3`  
		Last Modified: Wed, 11 Oct 2023 19:53:48 GMT  
		Size: 23.6 MB (23588086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b6c2ba718a2e4c688d25c56a5ccd994c3d661135cec510532624c88d9120a0`  
		Last Modified: Thu, 12 Oct 2023 14:30:45 GMT  
		Size: 19.1 MB (19079557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df642945c62c789f355dc49ee06e4cf84cf254d0700d6ca01f983950a226a70`  
		Last Modified: Thu, 12 Oct 2023 14:30:43 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4afb876c2e72f426105b4e693c8d85f6abbd7a16d9b32fd024f966853fc8353a`  
		Last Modified: Thu, 12 Oct 2023 14:30:50 GMT  
		Size: 50.0 MB (49958610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4396b0321f3b9b0da919f9248cf5d9ba9a3795bad0d0dd1b0916b4f269ed3ea4`  
		Last Modified: Thu, 12 Oct 2023 14:30:43 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.27.4-alpine`

```console
$ docker pull telegraf@sha256:f77ed7dddb02a84b5bdd31d9f89a018ee08edea598b7da9dd81e5d66577f651b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.27.4-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:6eccd860212b44034872f6130348edf970d72a900afcbafd229208de4d29b9d2
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61199653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48fd08420a9d1b3991e3781cda8fb3b5c38d0211c2fef5fef53881f9389ef80`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:41:50 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:42:00 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:42:01 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:42:01 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:42:01 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:42:01 GMT
CMD ["telegraf"]
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
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450dcdf691f11f970afef73d942c63e6161a568b77622ff4107e6478725af37c`  
		Last Modified: Sat, 21 Oct 2023 03:42:59 GMT  
		Size: 55.2 MB (55152107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102b1a74ea9501518451d0ae11db2bee8fe1b66599de184e0ea725f93b37782e`  
		Last Modified: Sat, 21 Oct 2023 03:42:50 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.27.4-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:b4e52a8cd5440d35e1009c242974397bdcc55a2a50066ed33ab4fddcc7e01b93
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55801017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d412a0494e0a1ec188214fe6a98c9bad9ded0972205b6354751f16585a8e3f3d`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:22 GMT
ENV TELEGRAF_VERSION=1.27.4
# Sat, 21 Oct 2023 03:05:31 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:32 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:32 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:32 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:32 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ef6f17a9a0ea6e7a97c008cc018d7359892e7edc9648fa9028a0c8f9ca1174`  
		Last Modified: Sat, 21 Oct 2023 03:06:25 GMT  
		Size: 49.8 MB (49795386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab157c6d650bcef23423e9caf5874f8b88eab7ddf83f54c5acd6e656238c20a`  
		Last Modified: Sat, 21 Oct 2023 03:06:19 GMT  
		Size: 328.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28`

```console
$ docker pull telegraf@sha256:45044de12342a3e6605a2519cc1b9c9b5e5da7f80bf906121155f852744425fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28` - linux; amd64

```console
$ docker pull telegraf@sha256:ae8d04a98fa87decb8eaedc776b64e2b638abf24f49c8df6e88b935454ffdedf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149428934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba3223aff3255094496c76f494ec8478a4345a41fcd33a5610d193c53e8ead5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:19:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 11:11:51 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 11:11:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 11:11:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 11:11:57 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 11:11:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 11:11:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc26d841b4acc2562483bf393ce1cf8bc358ced09ccd825425226827c79c92`  
		Last Modified: Thu, 12 Oct 2023 03:28:45 GMT  
		Size: 24.1 MB (24051259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42938defa8a6b527ab4fb0f8be74ac2b7c945f5518627ce9e869533ce2c3050`  
		Last Modified: Thu, 12 Oct 2023 11:12:37 GMT  
		Size: 19.1 MB (19145561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366994b97c2f17c0fe06554587854beea020e47b89b927da0bd69563cf6e7495`  
		Last Modified: Thu, 12 Oct 2023 11:12:33 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e103241e17d2011bccf621ea4ddd925f72e5d8edd72937ff0541a91adbf02ac`  
		Last Modified: Thu, 12 Oct 2023 11:13:01 GMT  
		Size: 56.6 MB (56647733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde8245dab2b08dfe26c20d1bad407015876943f7da2b81965b10a7721094714`  
		Last Modified: Thu, 12 Oct 2023 11:12:52 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2f21c884f8d65db4ac0103c0396c2df85fc6e969ac391911aefc751396c9ffce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137292642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63e497114b1ea2af819cc7f7d1fae6cd8d68bf20d24f0e8d454d5cdfde00c08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:59 GMT
ADD file:914e8a43f38c44fe9a6aabf05bbf3ebad5530966a354c8e7bb873c0842d35256 in / 
# Wed, 11 Oct 2023 17:42:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:45:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 18:09:40 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 18:09:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 18:09:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 18:09:47 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 18:09:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 18:09:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:65b9f3344eccdad2292cc7eec885befe05a52ec1136e145130c849441428eee6`  
		Last Modified: Wed, 11 Oct 2023 17:45:56 GMT  
		Size: 45.2 MB (45180287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbdddb82776e8c5901a821d5034c82b0fcba2993014440cd080d0592cd49616`  
		Last Modified: Thu, 12 Oct 2023 03:55:58 GMT  
		Size: 22.0 MB (21953833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fd75bac7be32a4c2229f7c55dc64abed60b0a8cb9e2fdd864034a57600f2fa`  
		Last Modified: Thu, 12 Oct 2023 18:10:18 GMT  
		Size: 18.0 MB (17991786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c42367e4c938159668542b19b5ed09bc2b4b58ea053c02eebd94a8f50a3210`  
		Last Modified: Thu, 12 Oct 2023 18:10:15 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d6b54cd32daf41ca19acc8ed79145806be6eabb7a400c70033de1be06da440`  
		Last Modified: Thu, 12 Oct 2023 18:10:41 GMT  
		Size: 52.2 MB (52164579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f18564885a3233532f9bd54ffbca067bae34b43ed72eebb50dcc2197463967`  
		Last Modified: Thu, 12 Oct 2023 18:10:32 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:96a630e45187dfa4035c540ce59f3d729bc08140c411fdbd3a23d46f015b3c72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143625843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f8ba7295ff8c8d7cf88952c6f1347e37fab93ec641bf6b73cbb95a1a78442`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:44:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 14:30:06 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 14:30:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 14:30:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 14:30:13 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 14:30:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 14:30:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7541d83e7b8c0f5f6cacacddfcf5fdd942793f13418bc4645203b4ab4f3de3`  
		Last Modified: Wed, 11 Oct 2023 19:53:48 GMT  
		Size: 23.6 MB (23588086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b6c2ba718a2e4c688d25c56a5ccd994c3d661135cec510532624c88d9120a0`  
		Last Modified: Thu, 12 Oct 2023 14:30:45 GMT  
		Size: 19.1 MB (19079557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df642945c62c789f355dc49ee06e4cf84cf254d0700d6ca01f983950a226a70`  
		Last Modified: Thu, 12 Oct 2023 14:30:43 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30efd171798f39f5eb511b22ad9fde2bc5ac5e8462442c891518ec4590f0f93f`  
		Last Modified: Thu, 12 Oct 2023 14:31:05 GMT  
		Size: 51.3 MB (51343464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc831cfc69832623b4b73a1f5a4d8a8d14fb14c9b44e6bec9ef4309840ee388`  
		Last Modified: Thu, 12 Oct 2023 14:30:59 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28-alpine`

```console
$ docker pull telegraf@sha256:ba402f6e3fc98fd48eb8070f73b5b66224eb01030e4a614cf6a4278d6984585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:69bebd7c809fcb80dae5cb32415c0e6cc6d2455d5b9b8a19aa4b3929ed5639b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62521037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525f48fc3aa884cb768faac6276ab3617f11afc108e6fdadfc0aee92116e2de9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:42:08 GMT
ENV TELEGRAF_VERSION=1.28.2
# Sat, 21 Oct 2023 03:42:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:42:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:42:15 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:42:16 GMT
CMD ["telegraf"]
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
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a8e7ab6adbaa2ebdebbf2f90e60f38083e73df4709f93c997f466cda88cf8`  
		Last Modified: Sat, 21 Oct 2023 03:43:18 GMT  
		Size: 56.5 MB (56473490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f03f2cd552260f6a9e153f1d7a2cd8d20f42a75c82678257440437c8063f02d`  
		Last Modified: Sat, 21 Oct 2023 03:43:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77ba9e2db7288643d9afc1ece48804538959fc09435ff47845fd592eb931de5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57166451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d231738b7dbaa1ae4efd5c04a72e092734d3854ca02139690876efea773b0c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:38 GMT
ENV TELEGRAF_VERSION=1.28.2
# Sat, 21 Oct 2023 03:05:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:48 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a03d0c1c9f911c0c46388757812fe06b7a28b0d9105172616fb0f937fee752`  
		Last Modified: Sat, 21 Oct 2023 03:06:41 GMT  
		Size: 51.2 MB (51160822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8092ff33c8ba83af3ec3266b7208acbb88006c9bf1bcef0e51d8ab9039e8b93`  
		Last Modified: Sat, 21 Oct 2023 03:06:34 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.2`

```console
$ docker pull telegraf@sha256:45044de12342a3e6605a2519cc1b9c9b5e5da7f80bf906121155f852744425fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:1.28.2` - linux; amd64

```console
$ docker pull telegraf@sha256:ae8d04a98fa87decb8eaedc776b64e2b638abf24f49c8df6e88b935454ffdedf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149428934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba3223aff3255094496c76f494ec8478a4345a41fcd33a5610d193c53e8ead5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:19:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 11:11:51 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 11:11:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 11:11:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 11:11:57 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 11:11:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 11:11:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc26d841b4acc2562483bf393ce1cf8bc358ced09ccd825425226827c79c92`  
		Last Modified: Thu, 12 Oct 2023 03:28:45 GMT  
		Size: 24.1 MB (24051259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42938defa8a6b527ab4fb0f8be74ac2b7c945f5518627ce9e869533ce2c3050`  
		Last Modified: Thu, 12 Oct 2023 11:12:37 GMT  
		Size: 19.1 MB (19145561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366994b97c2f17c0fe06554587854beea020e47b89b927da0bd69563cf6e7495`  
		Last Modified: Thu, 12 Oct 2023 11:12:33 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e103241e17d2011bccf621ea4ddd925f72e5d8edd72937ff0541a91adbf02ac`  
		Last Modified: Thu, 12 Oct 2023 11:13:01 GMT  
		Size: 56.6 MB (56647733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde8245dab2b08dfe26c20d1bad407015876943f7da2b81965b10a7721094714`  
		Last Modified: Thu, 12 Oct 2023 11:12:52 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.2` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2f21c884f8d65db4ac0103c0396c2df85fc6e969ac391911aefc751396c9ffce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137292642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63e497114b1ea2af819cc7f7d1fae6cd8d68bf20d24f0e8d454d5cdfde00c08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:59 GMT
ADD file:914e8a43f38c44fe9a6aabf05bbf3ebad5530966a354c8e7bb873c0842d35256 in / 
# Wed, 11 Oct 2023 17:42:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:45:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 18:09:40 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 18:09:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 18:09:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 18:09:47 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 18:09:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 18:09:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:65b9f3344eccdad2292cc7eec885befe05a52ec1136e145130c849441428eee6`  
		Last Modified: Wed, 11 Oct 2023 17:45:56 GMT  
		Size: 45.2 MB (45180287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbdddb82776e8c5901a821d5034c82b0fcba2993014440cd080d0592cd49616`  
		Last Modified: Thu, 12 Oct 2023 03:55:58 GMT  
		Size: 22.0 MB (21953833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fd75bac7be32a4c2229f7c55dc64abed60b0a8cb9e2fdd864034a57600f2fa`  
		Last Modified: Thu, 12 Oct 2023 18:10:18 GMT  
		Size: 18.0 MB (17991786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c42367e4c938159668542b19b5ed09bc2b4b58ea053c02eebd94a8f50a3210`  
		Last Modified: Thu, 12 Oct 2023 18:10:15 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d6b54cd32daf41ca19acc8ed79145806be6eabb7a400c70033de1be06da440`  
		Last Modified: Thu, 12 Oct 2023 18:10:41 GMT  
		Size: 52.2 MB (52164579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f18564885a3233532f9bd54ffbca067bae34b43ed72eebb50dcc2197463967`  
		Last Modified: Thu, 12 Oct 2023 18:10:32 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.2` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:96a630e45187dfa4035c540ce59f3d729bc08140c411fdbd3a23d46f015b3c72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143625843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f8ba7295ff8c8d7cf88952c6f1347e37fab93ec641bf6b73cbb95a1a78442`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:44:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 14:30:06 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 14:30:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 14:30:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 14:30:13 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 14:30:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 14:30:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7541d83e7b8c0f5f6cacacddfcf5fdd942793f13418bc4645203b4ab4f3de3`  
		Last Modified: Wed, 11 Oct 2023 19:53:48 GMT  
		Size: 23.6 MB (23588086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b6c2ba718a2e4c688d25c56a5ccd994c3d661135cec510532624c88d9120a0`  
		Last Modified: Thu, 12 Oct 2023 14:30:45 GMT  
		Size: 19.1 MB (19079557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df642945c62c789f355dc49ee06e4cf84cf254d0700d6ca01f983950a226a70`  
		Last Modified: Thu, 12 Oct 2023 14:30:43 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30efd171798f39f5eb511b22ad9fde2bc5ac5e8462442c891518ec4590f0f93f`  
		Last Modified: Thu, 12 Oct 2023 14:31:05 GMT  
		Size: 51.3 MB (51343464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc831cfc69832623b4b73a1f5a4d8a8d14fb14c9b44e6bec9ef4309840ee388`  
		Last Modified: Thu, 12 Oct 2023 14:30:59 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:1.28.2-alpine`

```console
$ docker pull telegraf@sha256:ba402f6e3fc98fd48eb8070f73b5b66224eb01030e4a614cf6a4278d6984585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:1.28.2-alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:69bebd7c809fcb80dae5cb32415c0e6cc6d2455d5b9b8a19aa4b3929ed5639b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62521037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525f48fc3aa884cb768faac6276ab3617f11afc108e6fdadfc0aee92116e2de9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:42:08 GMT
ENV TELEGRAF_VERSION=1.28.2
# Sat, 21 Oct 2023 03:42:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:42:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:42:15 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:42:16 GMT
CMD ["telegraf"]
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
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a8e7ab6adbaa2ebdebbf2f90e60f38083e73df4709f93c997f466cda88cf8`  
		Last Modified: Sat, 21 Oct 2023 03:43:18 GMT  
		Size: 56.5 MB (56473490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f03f2cd552260f6a9e153f1d7a2cd8d20f42a75c82678257440437c8063f02d`  
		Last Modified: Sat, 21 Oct 2023 03:43:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:1.28.2-alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77ba9e2db7288643d9afc1ece48804538959fc09435ff47845fd592eb931de5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57166451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d231738b7dbaa1ae4efd5c04a72e092734d3854ca02139690876efea773b0c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:38 GMT
ENV TELEGRAF_VERSION=1.28.2
# Sat, 21 Oct 2023 03:05:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:48 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a03d0c1c9f911c0c46388757812fe06b7a28b0d9105172616fb0f937fee752`  
		Last Modified: Sat, 21 Oct 2023 03:06:41 GMT  
		Size: 51.2 MB (51160822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8092ff33c8ba83af3ec3266b7208acbb88006c9bf1bcef0e51d8ab9039e8b93`  
		Last Modified: Sat, 21 Oct 2023 03:06:34 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:alpine`

```console
$ docker pull telegraf@sha256:ba402f6e3fc98fd48eb8070f73b5b66224eb01030e4a614cf6a4278d6984585a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `telegraf:alpine` - linux; amd64

```console
$ docker pull telegraf@sha256:69bebd7c809fcb80dae5cb32415c0e6cc6d2455d5b9b8a19aa4b3929ed5639b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.5 MB (62521037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:525f48fc3aa884cb768faac6276ab3617f11afc108e6fdadfc0aee92116e2de9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 01:30:37 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:41:50 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:42:08 GMT
ENV TELEGRAF_VERSION=1.28.2
# Sat, 21 Oct 2023 03:42:15 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:42:15 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:42:15 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:42:16 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:42:16 GMT
CMD ["telegraf"]
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
	-	`sha256:ba00d64dccafdbc853dd8b93a8277f727ce3f033368e6501a6bd8e5d8146745a`  
		Last Modified: Sat, 21 Oct 2023 03:42:51 GMT  
		Size: 2.6 MB (2644972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef9a8e7ab6adbaa2ebdebbf2f90e60f38083e73df4709f93c997f466cda88cf8`  
		Last Modified: Sat, 21 Oct 2023 03:43:18 GMT  
		Size: 56.5 MB (56473490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f03f2cd552260f6a9e153f1d7a2cd8d20f42a75c82678257440437c8063f02d`  
		Last Modified: Sat, 21 Oct 2023 03:43:09 GMT  
		Size: 327.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:alpine` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:77ba9e2db7288643d9afc1ece48804538959fc09435ff47845fd592eb931de5e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57166451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d231738b7dbaa1ae4efd5c04a72e092734d3854ca02139690876efea773b0c3`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Tue, 17 Oct 2023 00:43:51 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf
# Sat, 21 Oct 2023 03:05:22 GMT
RUN apk add --no-cache iputils ca-certificates net-snmp-tools procps lm_sensors tzdata su-exec libcap &&     update-ca-certificates
# Sat, 21 Oct 2023 03:05:38 GMT
ENV TELEGRAF_VERSION=1.28.2
# Sat, 21 Oct 2023 03:05:47 GMT
RUN ARCH= &&     case "$(apk --print-arch)" in         x86_64) ARCH='amd64';;         aarch64) ARCH='arm64';;         *) echo "Unsupported architecture: $(apk --print-arch)"; exit 1;;     esac &&     set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     gpg --batch --verify telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz.asc telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mkdir -p /usr/src /etc/telegraf &&     tar -C /usr/src -xzf telegraf-${TELEGRAF_VERSION}_linux_${ARCH}.tar.gz &&     mv /usr/src/telegraf*/etc/telegraf/telegraf.conf /etc/telegraf/ &&     mkdir /etc/telegraf/telegraf.d &&     cp -a /usr/src/telegraf*/usr/bin/telegraf /usr/bin/ &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S telegraf &&     adduser -S telegraf -G telegraf &&     chown -R telegraf:telegraf /etc/telegraf
# Sat, 21 Oct 2023 03:05:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Sat, 21 Oct 2023 03:05:48 GMT
COPY file:f41cb64129e03c46523c3acd2da77376a68d9785d775faf0d359051c20b4f1bf in /entrypoint.sh 
# Sat, 21 Oct 2023 03:05:48 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Sat, 21 Oct 2023 03:05:48 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e248ba14d9e254569a72ce1316c31cb26327474bc388ccd8fbd2fa78078db3aa`  
		Last Modified: Tue, 17 Oct 2023 00:44:22 GMT  
		Size: 278.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df4f9000c980c4ebf3511e8960492d4efd4c2527f058385ee1575fdb80c0cea7`  
		Last Modified: Sat, 21 Oct 2023 03:06:20 GMT  
		Size: 2.7 MB (2673194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27a03d0c1c9f911c0c46388757812fe06b7a28b0d9105172616fb0f937fee752`  
		Last Modified: Sat, 21 Oct 2023 03:06:41 GMT  
		Size: 51.2 MB (51160822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8092ff33c8ba83af3ec3266b7208acbb88006c9bf1bcef0e51d8ab9039e8b93`  
		Last Modified: Sat, 21 Oct 2023 03:06:34 GMT  
		Size: 326.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `telegraf:latest`

```console
$ docker pull telegraf@sha256:45044de12342a3e6605a2519cc1b9c9b5e5da7f80bf906121155f852744425fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:ae8d04a98fa87decb8eaedc776b64e2b638abf24f49c8df6e88b935454ffdedf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149428934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fba3223aff3255094496c76f494ec8478a4345a41fcd33a5610d193c53e8ead5`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:19:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:37 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 11:11:38 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 11:11:51 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 11:11:56 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 11:11:56 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 11:11:57 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 11:11:57 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 11:11:57 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ccc26d841b4acc2562483bf393ce1cf8bc358ced09ccd825425226827c79c92`  
		Last Modified: Thu, 12 Oct 2023 03:28:45 GMT  
		Size: 24.1 MB (24051259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b42938defa8a6b527ab4fb0f8be74ac2b7c945f5518627ce9e869533ce2c3050`  
		Last Modified: Thu, 12 Oct 2023 11:12:37 GMT  
		Size: 19.1 MB (19145561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:366994b97c2f17c0fe06554587854beea020e47b89b927da0bd69563cf6e7495`  
		Last Modified: Thu, 12 Oct 2023 11:12:33 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e103241e17d2011bccf621ea4ddd925f72e5d8edd72937ff0541a91adbf02ac`  
		Last Modified: Thu, 12 Oct 2023 11:13:01 GMT  
		Size: 56.6 MB (56647733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dde8245dab2b08dfe26c20d1bad407015876943f7da2b81965b10a7721094714`  
		Last Modified: Thu, 12 Oct 2023 11:12:52 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:2f21c884f8d65db4ac0103c0396c2df85fc6e969ac391911aefc751396c9ffce
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.3 MB (137292642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e63e497114b1ea2af819cc7f7d1fae6cd8d68bf20d24f0e8d454d5cdfde00c08`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 17:41:59 GMT
ADD file:914e8a43f38c44fe9a6aabf05bbf3ebad5530966a354c8e7bb873c0842d35256 in / 
# Wed, 11 Oct 2023 17:42:00 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:45:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:26 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 18:09:27 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 18:09:40 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 18:09:46 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 18:09:47 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 18:09:47 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 18:09:47 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 18:09:47 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:65b9f3344eccdad2292cc7eec885befe05a52ec1136e145130c849441428eee6`  
		Last Modified: Wed, 11 Oct 2023 17:45:56 GMT  
		Size: 45.2 MB (45180287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbdddb82776e8c5901a821d5034c82b0fcba2993014440cd080d0592cd49616`  
		Last Modified: Thu, 12 Oct 2023 03:55:58 GMT  
		Size: 22.0 MB (21953833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fd75bac7be32a4c2229f7c55dc64abed60b0a8cb9e2fdd864034a57600f2fa`  
		Last Modified: Thu, 12 Oct 2023 18:10:18 GMT  
		Size: 18.0 MB (17991786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86c42367e4c938159668542b19b5ed09bc2b4b58ea053c02eebd94a8f50a3210`  
		Last Modified: Thu, 12 Oct 2023 18:10:15 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47d6b54cd32daf41ca19acc8ed79145806be6eabb7a400c70033de1be06da440`  
		Last Modified: Thu, 12 Oct 2023 18:10:41 GMT  
		Size: 52.2 MB (52164579 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85f18564885a3233532f9bd54ffbca067bae34b43ed72eebb50dcc2197463967`  
		Last Modified: Thu, 12 Oct 2023 18:10:32 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:96a630e45187dfa4035c540ce59f3d729bc08140c411fdbd3a23d46f015b3c72
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143625843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10f8ba7295ff8c8d7cf88952c6f1347e37fab93ec641bf6b73cbb95a1a78442`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 19:44:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:52 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors libcap2-bin &&     rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 14:29:53 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Thu, 12 Oct 2023 14:30:06 GMT
ENV TELEGRAF_VERSION=1.28.2
# Thu, 12 Oct 2023 14:30:12 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Thu, 12 Oct 2023 14:30:13 GMT
EXPOSE 8092/udp 8094 8125/udp
# Thu, 12 Oct 2023 14:30:13 GMT
COPY file:689e73cc90c23fa6e27f7d087886e186b6baf02bb95756b42136644d4f83a893 in /entrypoint.sh 
# Thu, 12 Oct 2023 14:30:13 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Oct 2023 14:30:13 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b7541d83e7b8c0f5f6cacacddfcf5fdd942793f13418bc4645203b4ab4f3de3`  
		Last Modified: Wed, 11 Oct 2023 19:53:48 GMT  
		Size: 23.6 MB (23588086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b6c2ba718a2e4c688d25c56a5ccd994c3d661135cec510532624c88d9120a0`  
		Last Modified: Thu, 12 Oct 2023 14:30:45 GMT  
		Size: 19.1 MB (19079557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8df642945c62c789f355dc49ee06e4cf84cf254d0700d6ca01f983950a226a70`  
		Last Modified: Thu, 12 Oct 2023 14:30:43 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30efd171798f39f5eb511b22ad9fde2bc5ac5e8462442c891518ec4590f0f93f`  
		Last Modified: Thu, 12 Oct 2023 14:31:05 GMT  
		Size: 51.3 MB (51343464 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fc831cfc69832623b4b73a1f5a4d8a8d14fb14c9b44e6bec9ef4309840ee388`  
		Last Modified: Thu, 12 Oct 2023 14:30:59 GMT  
		Size: 343.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
