## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:f5198ca7a64fef6bf10e1d49644f748c2a5e851deed064b74428c1fb59b4af24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:641d7cf97f9d996310b0a59a30dc3ce2fc618d58a40e0642607d7b8535f5fafb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **111.5 MB (111543257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e383abfa09d5df0474262098a4a9a4668880887e02be9dbcf8b3fe223be575`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 23 Jun 2021 00:21:59 GMT
ADD file:899a3c031d50263e5fce253aef92e05aec77f14ec3c38a37f08414e4c9b358f2 in / 
# Wed, 23 Jun 2021 00:22:00 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:56:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 00:56:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 24 Jun 2021 01:37:50 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 24 Jun 2021 01:37:54 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 24 Jun 2021 01:38:06 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 24 Jun 2021 01:38:09 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 24 Jun 2021 01:38:10 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 24 Jun 2021 01:38:10 GMT
EXPOSE 9092
# Thu, 24 Jun 2021 01:38:10 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 24 Jun 2021 01:38:10 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 24 Jun 2021 01:38:11 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 24 Jun 2021 01:38:11 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:199ebcd83264652823564822c7ef553db971042e35d7f347f66ea8a60a480545`  
		Last Modified: Wed, 23 Jun 2021 00:28:01 GMT  
		Size: 45.4 MB (45379993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddbb155879c013b8bb809e63f37f6dae34e890ec41f5a108d57f0958ca7365bf`  
		Last Modified: Wed, 23 Jun 2021 01:04:33 GMT  
		Size: 11.3 MB (11294536 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c194bbaa3d8bb7beb2bbbf9e74fc0fa7b6354f836402482f35b408c9163c5792`  
		Last Modified: Wed, 23 Jun 2021 01:04:32 GMT  
		Size: 4.3 MB (4342418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3484d0bf55eaf0f7d4a753065108b151f460c824f3e443d9412e141be8bc7277`  
		Last Modified: Thu, 24 Jun 2021 01:38:33 GMT  
		Size: 13.3 MB (13303741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4012297e2093eaf38b3dcae2aa99d2d2e73cad67adf440b6d7ce91fb0ea0ba`  
		Last Modified: Thu, 24 Jun 2021 01:38:31 GMT  
		Size: 2.9 KB (2855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a6ab4059ff792b9f3aed5b88d93e3833074ed427948ab745b058f0e4a9fdd6f`  
		Last Modified: Thu, 24 Jun 2021 01:38:53 GMT  
		Size: 37.2 MB (37219260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de745691f278f750ee337d8abbbf87c5e4f2b99b66bdeabf1e055dd280634246`  
		Last Modified: Thu, 24 Jun 2021 01:38:48 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:771dbed37f4d0e88b40232451fc8479a5192c9a500b67ba8e9963bd1807a4cbb`  
		Last Modified: Thu, 24 Jun 2021 01:38:48 GMT  
		Size: 228.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm variant v7

```console
$ docker pull kapacitor@sha256:11b893a390d4f14d475156d2316c008d3aad37aa488772ef7e5b367f03c20b63
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.3 MB (104253572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d7b614afc4796360163f90f0be676ab2bc192d6aa5ea0fd6fd80d1437904588`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Wed, 12 May 2021 01:11:51 GMT
ADD file:81cfd4e746bdfcc19847240b77012487652be22dbd5741ccb2485a4207f2b73f in / 
# Wed, 12 May 2021 01:11:56 GMT
CMD ["bash"]
# Thu, 27 May 2021 00:45:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 27 May 2021 00:45:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 27 May 2021 15:24:13 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Thu, 27 May 2021 15:24:16 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Thu, 27 May 2021 15:24:29 GMT
ENV KAPACITOR_VERSION=1.5.9
# Thu, 27 May 2021 15:24:33 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Thu, 27 May 2021 15:24:34 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Thu, 27 May 2021 15:24:34 GMT
EXPOSE 9092
# Thu, 27 May 2021 15:24:34 GMT
VOLUME [/var/lib/kapacitor]
# Thu, 27 May 2021 15:24:34 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Thu, 27 May 2021 15:24:35 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 27 May 2021 15:24:35 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:55b9a6b6b2552c5b2eac0a316e75a7bc18092819ee25c4f1d4d54700bcc1d3dc`  
		Last Modified: Wed, 12 May 2021 01:21:23 GMT  
		Size: 42.1 MB (42120307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba756a0ca8996787a145d62543ecf7cec523a638705be132f442d2013655149`  
		Last Modified: Thu, 27 May 2021 01:06:39 GMT  
		Size: 10.0 MB (9950803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c61945aef6a8fee06fbe4dccead7cbad9da46ba174cee1eae1f813541ddb76b3`  
		Last Modified: Thu, 27 May 2021 01:06:38 GMT  
		Size: 3.9 MB (3921169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73f0caaed9872f09cfec75a2a6ae01a4bf47adb5f7bad5d63bb822f235fa7538`  
		Last Modified: Thu, 27 May 2021 15:25:04 GMT  
		Size: 13.5 MB (13471332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16f7b135b7305744606fa4269bd800266ba98474e8d1448b372418d65dbd28fc`  
		Last Modified: Thu, 27 May 2021 15:25:01 GMT  
		Size: 2.9 KB (2853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc129f582c7b2ad5e74a23eb114991e4437fadd5f5f0b563da5736e6fe8704a`  
		Last Modified: Thu, 27 May 2021 15:25:27 GMT  
		Size: 34.8 MB (34786652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69dc39b8bac4be3a50381a992e2a62fa2da54b90031d9790fe3e7c60c13caa99`  
		Last Modified: Thu, 27 May 2021 15:25:21 GMT  
		Size: 224.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36170f3dbd5926adbbaef991792135405c512502786fc88dbfc7fc91f16fb8fe`  
		Last Modified: Thu, 27 May 2021 15:25:21 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:24dfe8ac7fca92649bb754592134fa03fd39b60c2a8bc5308b310527df24ad0b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.1 MB (105059188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fca6192994de70947ed75db98334f8a3c6336ee728eae3131ef3472393da040`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 22 Jun 2021 23:50:55 GMT
ADD file:02285d0bd3ea996a7ebbe069a83e508701cbaf14f53fdeaa123775acd7e0537f in / 
# Tue, 22 Jun 2021 23:50:56 GMT
CMD ["bash"]
# Wed, 23 Jun 2021 00:27:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		apt-transport-https 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 23 Jun 2021 00:27:33 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 23 Jun 2021 18:30:27 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc
# Wed, 23 Jun 2021 18:30:30 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     for key in         05CE15085FC09D18E99EFB22684A14CF2582E0C5 ;     do         gpg --keyserver ha.pool.sks-keyservers.net --recv-keys "$key" ||         gpg --keyserver pgp.mit.edu --recv-keys "$key" ||         gpg --keyserver keyserver.pgp.com --recv-keys "$key" ;     done
# Wed, 23 Jun 2021 18:30:40 GMT
ENV KAPACITOR_VERSION=1.5.9
# Wed, 23 Jun 2021 18:30:43 GMT
RUN ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in       amd64) ARCH='amd64';;       arm64) ARCH='arm64';;       armhf) ARCH='armhf';;       armel) ARCH='armel';;       *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb*
# Wed, 23 Jun 2021 18:30:43 GMT
COPY file:9450c5dcbc0a583243f987f682dc6c44d9e4a3f1c31d1bb9957f313457e444ec in /etc/kapacitor/kapacitor.conf 
# Wed, 23 Jun 2021 18:30:43 GMT
EXPOSE 9092
# Wed, 23 Jun 2021 18:30:44 GMT
VOLUME [/var/lib/kapacitor]
# Wed, 23 Jun 2021 18:30:44 GMT
COPY file:a229567085df49450fcc70ed6d49efcbdfc41ca92b6c5bdb3b541cb803165dbc in /entrypoint.sh 
# Wed, 23 Jun 2021 18:30:44 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Wed, 23 Jun 2021 18:30:44 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:0789e4a342a11c7c57a241829a41af53fbd194e6dede60c6d6f63d69e403b2cd`  
		Last Modified: Tue, 22 Jun 2021 23:57:52 GMT  
		Size: 43.2 MB (43177421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfd2ed69368e8a7d296f1c91060e897753bed4a79ab68ed47c544e1f4d6fadcd`  
		Last Modified: Wed, 23 Jun 2021 00:35:58 GMT  
		Size: 10.2 MB (10214577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c76e514669ff971481e0d19dc0581f90d72eab2d0e117a5761ae016e14f213`  
		Last Modified: Wed, 23 Jun 2021 00:35:57 GMT  
		Size: 4.1 MB (4096534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b2de4768a1c15ce3980cc7ad3cb98882f89999a553fb1328ee0ea58ca1a1a22`  
		Last Modified: Wed, 23 Jun 2021 18:31:05 GMT  
		Size: 13.0 MB (13006392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae8c40d5b6ee697f7d91f741516f12b3b77ba2e7f2659cf27640152496aef83`  
		Last Modified: Wed, 23 Jun 2021 18:31:03 GMT  
		Size: 2.9 KB (2854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271cc6c4cc1d0584ef6813f00a7465e15d77ba403296321f11c6be76a8dea274`  
		Last Modified: Wed, 23 Jun 2021 18:31:25 GMT  
		Size: 34.6 MB (34560953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a251bef91330d334e7f4ae9ccf4cdcc9f097b48744320a9d0c7405e3b019458f`  
		Last Modified: Wed, 23 Jun 2021 18:31:20 GMT  
		Size: 226.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e75f9e176592ceb800838fbf17f5bbc3417520f888ced9d4f01288e462f6acd`  
		Last Modified: Wed, 23 Jun 2021 18:31:20 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
