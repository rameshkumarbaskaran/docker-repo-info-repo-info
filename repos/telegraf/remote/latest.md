## `telegraf:latest`

```console
$ docker pull telegraf@sha256:879ccdec91a2575c540c6b1990bd8bdc30441cfafdb19826600a7e639c3da898
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `telegraf:latest` - linux; amd64

```console
$ docker pull telegraf@sha256:210d82542b241a9d68c3f93b3b8549ed35d09c1f1eed4d6067971031361dbed7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **121.3 MB (121294336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c905645a69ca67570c85da3008b46b7f23bc59847c17189dff073cbf542dffb`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:53 GMT
ADD file:98c256057b79b141aea9a806a4538cf6c3f340d7e3b0d6e8c363699333f3406b in / 
# Tue, 12 Oct 2021 01:20:53 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 15:44:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 15:44:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 10:25:38 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 10:25:46 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 01:31:43 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 01:31:47 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 01:31:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:44:38 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:44:39 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:44:39 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:07471e81507f7cf1100827f10c60c3c0422d1222430e34e527d97ec72b14a193`  
		Last Modified: Tue, 12 Oct 2021 01:26:26 GMT  
		Size: 50.4 MB (50436692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cef1aa2170c001b320769bf8b018ed82d2c94a673e3010ea1ffe152e107419`  
		Last Modified: Tue, 12 Oct 2021 15:54:16 GMT  
		Size: 7.8 MB (7833862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13a51f13be8e69cfc526b671d0bbf621b985b0932acd1523050e2995777b5926`  
		Last Modified: Tue, 12 Oct 2021 15:54:17 GMT  
		Size: 10.0 MB (9997204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c91a466291d423e3faad6a8be6ae82e4a4d0550acb67989ac71c98f900e74d41`  
		Last Modified: Wed, 13 Oct 2021 10:26:55 GMT  
		Size: 17.4 MB (17415387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b77934da0dce5bef46b239a3871787c2962a08cf1c8b1e629282f0c617b46426`  
		Last Modified: Wed, 13 Oct 2021 10:26:52 GMT  
		Size: 2.9 KB (2906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9bb9c78b7fc1c3d2d301570d7a073caa789bd48f29617a234431b3937566893`  
		Last Modified: Fri, 29 Oct 2021 01:33:18 GMT  
		Size: 35.6 MB (35608054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11f86ea74520d5c38238db95f3d83fc8da214f7a35f2cfef7399ea3b2944df12`  
		Last Modified: Wed, 03 Nov 2021 19:46:07 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm variant v7

```console
$ docker pull telegraf@sha256:fedd44d5aad17fa7b3ad65a823d2881ad75014b2d295dc49ce175c370811ec16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.6 MB (111628087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba02837fbe7cada0a9244a77c1ddf35335f1e0a5c217af935a9eff4f7b7f69`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Tue, 12 Oct 2021 01:29:06 GMT
ADD file:b1857dc4fe4fbc4af220829cc6af7169c4555d3f63a3a304db6fa0146b1d5539 in / 
# Tue, 12 Oct 2021 01:29:08 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 18:39:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 18:39:53 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 13 Oct 2021 15:31:00 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 15:31:08 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Fri, 29 Oct 2021 02:06:56 GMT
ENV TELEGRAF_VERSION=1.20.3
# Fri, 29 Oct 2021 02:07:08 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Fri, 29 Oct 2021 02:07:09 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 03 Nov 2021 19:51:49 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 03 Nov 2021 19:51:49 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 03 Nov 2021 19:51:50 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:139a906e9407e96c50669130c30fe8fba2681b14aa838a3e52f8753b566ef1c8`  
		Last Modified: Tue, 12 Oct 2021 01:45:13 GMT  
		Size: 45.9 MB (45917899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3907051e2154d5bd4ad15141b8938bc09674039787512494a99b93fd4ebc088d`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 7.1 MB (7125242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8651d4793d5f4d465002213d2d462c964aaf8665a87d5f9cc0de7384f10eeb10`  
		Last Modified: Tue, 12 Oct 2021 19:00:49 GMT  
		Size: 9.3 MB (9343819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e659684a04aace7b984a69bccde2a720cb53304f8905d65b9068605177b2a4b6`  
		Last Modified: Wed, 13 Oct 2021 15:33:06 GMT  
		Size: 16.2 MB (16161376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc86d346babddcb58c40b9188fc289d120a16518eed1782662459497e55f179`  
		Last Modified: Wed, 13 Oct 2021 15:32:54 GMT  
		Size: 2.9 KB (2905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:addd4dfa7b430b02958aab120dc5d6dd3133c1b1f527269a956ba4078dd4998a`  
		Last Modified: Fri, 29 Oct 2021 02:08:41 GMT  
		Size: 33.1 MB (33076615 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc2b4bc4eec6033093c06cf1bbeed8bd8ad73d8db305ce297557af064b7aaf22`  
		Last Modified: Wed, 03 Nov 2021 19:52:56 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `telegraf:latest` - linux; arm64 variant v8

```console
$ docker pull telegraf@sha256:59deb3510f567d7f1cd90aa511cff2b0abf9db2cdd0e1b4db6080b21488d6932
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **116.1 MB (116091267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec99cb94cc34397b9783c8ee0f16d8185ee216fa2cdccaf9361fc23b7cd01e54`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["telegraf"]`

```dockerfile
# Wed, 17 Nov 2021 02:40:27 GMT
ADD file:c7e9e884b1494f96e33e9d9a892b51367af8943edb282c4101cc99ea78a7753f in / 
# Wed, 17 Nov 2021 02:40:28 GMT
CMD ["bash"]
# Wed, 17 Nov 2021 13:28:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 13:28:15 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 17 Nov 2021 20:42:06 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends iputils-ping snmp procps lm-sensors &&     rm -rf /var/lib/apt/lists/*
# Wed, 17 Nov 2021 20:42:09 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done
# Wed, 17 Nov 2021 20:42:38 GMT
ENV TELEGRAF_VERSION=1.20.3
# Wed, 17 Nov 2021 20:42:48 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/telegraf/releases/telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb.asc telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     dpkg -i telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb &&     rm -f telegraf_${TELEGRAF_VERSION}-1_${ARCH}.deb*
# Wed, 17 Nov 2021 20:42:48 GMT
EXPOSE 8092/udp 8094 8125/udp
# Wed, 17 Nov 2021 20:42:50 GMT
COPY file:2b9e4cba82211388672f0396330a391806dce79d249e808afdc3d074ec98a210 in /entrypoint.sh 
# Wed, 17 Nov 2021 20:42:50 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 17 Nov 2021 20:42:51 GMT
CMD ["telegraf"]
```

-	Layers:
	-	`sha256:626979e62c56e192812e818d52b82f063d9f9514b1b7bae14e534e4a7c98117a`  
		Last Modified: Wed, 17 Nov 2021 02:47:40 GMT  
		Size: 49.2 MB (49222990 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:134a528370d5dcbf5b6ba2d8c20f576504448e8f2d1debb5d2a4950a38a3ff2d`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 7.7 MB (7695161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e12e3364b52ad043d8e79f750863ed4ca2878c4fdf45ded974508febc55fdd`  
		Last Modified: Wed, 17 Nov 2021 13:37:44 GMT  
		Size: 9.8 MB (9767133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be62c7c66899dfefa611452ca6b38510228e4e1661d1ec078d90733f59865bcb`  
		Last Modified: Wed, 17 Nov 2021 20:43:17 GMT  
		Size: 17.1 MB (17059007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ea9240a1fea313b800d353f9288154cce52bcb21b3cfabfc7bf0f861090de7`  
		Last Modified: Wed, 17 Nov 2021 20:43:14 GMT  
		Size: 2.9 KB (2875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b99ce1f5cf7a1e9e2a732004677c1cb2ececf45b1deb897dcb743554459076d`  
		Last Modified: Wed, 17 Nov 2021 20:43:52 GMT  
		Size: 32.3 MB (32343870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2613b76c3ec562d8153bf6a6a7985c744b76bcc06f5b20984803e3671449d2b`  
		Last Modified: Wed, 17 Nov 2021 20:43:46 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
