<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `nats`

-	[`nats:2`](#nats2)
-	[`nats:2-alpine`](#nats2-alpine)
-	[`nats:2-alpine3.15`](#nats2-alpine315)
-	[`nats:2-linux`](#nats2-linux)
-	[`nats:2-nanoserver`](#nats2-nanoserver)
-	[`nats:2-nanoserver-1809`](#nats2-nanoserver-1809)
-	[`nats:2-scratch`](#nats2-scratch)
-	[`nats:2-windowsservercore`](#nats2-windowsservercore)
-	[`nats:2-windowsservercore-1809`](#nats2-windowsservercore-1809)
-	[`nats:2.8`](#nats28)
-	[`nats:2.8-alpine`](#nats28-alpine)
-	[`nats:2.8-alpine3.15`](#nats28-alpine315)
-	[`nats:2.8-linux`](#nats28-linux)
-	[`nats:2.8-nanoserver`](#nats28-nanoserver)
-	[`nats:2.8-nanoserver-1809`](#nats28-nanoserver-1809)
-	[`nats:2.8-scratch`](#nats28-scratch)
-	[`nats:2.8-windowsservercore`](#nats28-windowsservercore)
-	[`nats:2.8-windowsservercore-1809`](#nats28-windowsservercore-1809)
-	[`nats:2.8.3`](#nats283)
-	[`nats:2.8.3-alpine`](#nats283-alpine)
-	[`nats:2.8.3-alpine3.15`](#nats283-alpine315)
-	[`nats:2.8.3-linux`](#nats283-linux)
-	[`nats:2.8.3-nanoserver`](#nats283-nanoserver)
-	[`nats:2.8.3-nanoserver-1809`](#nats283-nanoserver-1809)
-	[`nats:2.8.3-scratch`](#nats283-scratch)
-	[`nats:2.8.3-windowsservercore`](#nats283-windowsservercore)
-	[`nats:2.8.3-windowsservercore-1809`](#nats283-windowsservercore-1809)
-	[`nats:alpine`](#natsalpine)
-	[`nats:alpine3.15`](#natsalpine315)
-	[`nats:latest`](#natslatest)
-	[`nats:linux`](#natslinux)
-	[`nats:nanoserver`](#natsnanoserver)
-	[`nats:nanoserver-1809`](#natsnanoserver-1809)
-	[`nats:scratch`](#natsscratch)
-	[`nats:windowsservercore`](#natswindowsservercore)
-	[`nats:windowsservercore-1809`](#natswindowsservercore-1809)

## `nats:2`

```console
$ docker pull nats@sha256:c140d3e0949999f528dd57e016c34ee4916ede78f38a75a8c6f9c294f6d109ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

### `nats:2` - linux; amd64

```console
$ docker pull nats@sha256:c4c5aa8d8b2ce861febd7bd4dcd9a729204ba3f15f91fd96f45ab5a6e100e516
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca6ed6836bb8a2f8705608091864ce3c25b8ca32693003e2a8df04e30dc0f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 22:19:51 GMT
COPY file:8ff89c4fbf2c06b0c443f547e21c09f4d00bc37565795d87bfb43a04d4ff236e in /nats-server 
# Mon, 23 May 2022 22:19:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 22:19:51 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 22:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:49229864ce5450b6b5291aa946e418a9b56e6bbac1179c2a3ca592284b674f6c`  
		Last Modified: Mon, 23 May 2022 22:20:42 GMT  
		Size: 4.6 MB (4589871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f11a75312c73ef42e06951cc5acd4b2690648b1ab001bacda9622a11819993`  
		Last Modified: Mon, 23 May 2022 22:20:41 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:95b08fc423ab3d372702336dae5a8dbe2d1da429c18eeaf36f936fc0875ee7ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107772713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5d6c0f979e88d8401fee505a489498a7f206548060dfbf92e3adf4875a8ef8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 23 May 2022 22:16:52 GMT
RUN cmd /S /C #(nop) COPY file:20c5da4e402adeb74e59df38a88afb7f0706725d1cf47a32deba2a95222bf05e in C:\nats-server.exe 
# Mon, 23 May 2022 22:16:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 23 May 2022 22:16:55 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75ab9a5e0f44e79c3adfc8b401bd352612bfa1c195e182dfedca24907fc2cb`  
		Last Modified: Mon, 23 May 2022 22:17:51 GMT  
		Size: 4.6 MB (4632778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7d580b9477c406ac03b52996e543c4d98651c583032c1cc8a15b97a42974d0`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0c44352b5c88d59e36acd76446dfd0543670ed32caba214353a395b0e27590`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430a07615e58e42c48f51d89c04072d98127ea7db787f97cdef0385b134fe681`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272f4f628d52da760d5a41b2c254fe1082dbf88591529f520cc4d37a317a47`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine`

```console
$ docker pull nats@sha256:6ce50789c72aee8684c30383c8b49b80613cec2b81c61ed17f446a770fe6c705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2769de3270a9a86a1f799007cb1be2cbac229c07395206d13fbf845312481fc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0303f1d0cccc66a96da1353b9732b2b1b9dbd21206996b9af197b108e52d444b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Mon, 23 May 2022 22:19:43 GMT
ENV NATS_SERVER=2.8.3
# Mon, 23 May 2022 22:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='905df5647dba0443ce6b92116ff5c6ceb49d3e24fa78c999d0c19fe634f341d6' ;; 		armhf) natsArch='arm6'; sha256='590a0460362ab1fc47ebce8886f5a53ff8b91abefa412ce77762f8514041394b' ;; 		armv7) natsArch='arm7'; sha256='142673f4eafca832e0347b1be0f5f9b0b7b23a46c08a623b63c6925a94a2d9f1' ;; 		x86_64) natsArch='amd64'; sha256='16e6bfa14e8ba9bc7d924e296bfe6bcad803b04318e6d60ef14ee45e3d3ddc60' ;; 		x86) natsArch='386'; sha256='fc749ab7574aa9ae22661a89ad73ac26331772e2302197d1625db56e967a74ac' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 23 May 2022 22:19:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 23 May 2022 22:19:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 23 May 2022 22:19:45 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 22:19:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68886d04807b30a327d175e97fe6fa560a6f4e68ea614397e87e7d456d6ace19`  
		Last Modified: Mon, 23 May 2022 22:20:18 GMT  
		Size: 4.9 MB (4863157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfc1bf8ce728acff89f87564fb40e67def44a450bd0e29f09309dad99e81ac6`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c52785e040cd5cb0b784f0b7cf87f4ef40f0031383deb06acd3a5018bd0eee`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:12b766cef3be0b9dc70e35a9cefcecbfad16a19e00b94a4737134ebbee24ea31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cc5ce43b7fd2c1dc34d986696c64da1a158fc067f5a4710ce475ce2f10eaec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:01:15 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:01:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:01:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:01:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:01:21 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:01:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508da0a7a8c69badd89084de30d788f3c0bc57d625677ec7d68c32f18d466ba`  
		Last Modified: Wed, 04 May 2022 22:03:28 GMT  
		Size: 4.5 MB (4510625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7965b001731ee55e0b7b2c11c7ff5f851afaed57dba5ef2a08324fab5de994f7`  
		Last Modified: Wed, 04 May 2022 22:03:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d031fa4afb68088db4a684f2332c5c8c3ecedb55d2aee461d64c8556afb468`  
		Last Modified: Wed, 04 May 2022 22:03:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7d6c71099975b1e928511819a05612d582d412c5ed2838f04882514d0e77fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6930001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3813055a26f58efed9d97ad053203ba493589fa6e486f3dd5810354defc6b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:17:46 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:17:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:17:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:17:51 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:17:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3de3c7329a4a2fbd9e8c9cd595a837860930995c5a11d2459e045b8d2dab`  
		Last Modified: Wed, 04 May 2022 22:20:00 GMT  
		Size: 4.5 MB (4504680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc12ec06d594c70e53bb45c9912d27ad4869faf092615047ea9faab11d6ccb`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0c0af17ebf42f5af072c2b71c091af0b659ac5e20a80c92ca74da9ec5353d`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:81e20b06f2b5aac1ca438142975de9c05234b243fcb497ab8afd7f0bcd4a28a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2a5e86ad6fc84ed6f66fecfc26474466d0f61712b85aa012fc0b7e726019e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:48:24 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:48:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:48:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:48:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:48:29 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:48:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7ea9151b15b8e90d2a0ef58393de32cefb12a7f7c7e3d7a011808b38e59565`  
		Last Modified: Wed, 04 May 2022 21:49:31 GMT  
		Size: 4.5 MB (4490808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f800447a181fc7e3f37c2e68d8374347459e1d12a8d8c8653b7da45180ae97f`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f3b307d2ae2b261df9d763e886b3ae75f9aba6dc927eaf3f28cae9375c050`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-alpine3.15`

```console
$ docker pull nats@sha256:6ce50789c72aee8684c30383c8b49b80613cec2b81c61ed17f446a770fe6c705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:2769de3270a9a86a1f799007cb1be2cbac229c07395206d13fbf845312481fc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0303f1d0cccc66a96da1353b9732b2b1b9dbd21206996b9af197b108e52d444b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Mon, 23 May 2022 22:19:43 GMT
ENV NATS_SERVER=2.8.3
# Mon, 23 May 2022 22:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='905df5647dba0443ce6b92116ff5c6ceb49d3e24fa78c999d0c19fe634f341d6' ;; 		armhf) natsArch='arm6'; sha256='590a0460362ab1fc47ebce8886f5a53ff8b91abefa412ce77762f8514041394b' ;; 		armv7) natsArch='arm7'; sha256='142673f4eafca832e0347b1be0f5f9b0b7b23a46c08a623b63c6925a94a2d9f1' ;; 		x86_64) natsArch='amd64'; sha256='16e6bfa14e8ba9bc7d924e296bfe6bcad803b04318e6d60ef14ee45e3d3ddc60' ;; 		x86) natsArch='386'; sha256='fc749ab7574aa9ae22661a89ad73ac26331772e2302197d1625db56e967a74ac' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 23 May 2022 22:19:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 23 May 2022 22:19:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 23 May 2022 22:19:45 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 22:19:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68886d04807b30a327d175e97fe6fa560a6f4e68ea614397e87e7d456d6ace19`  
		Last Modified: Mon, 23 May 2022 22:20:18 GMT  
		Size: 4.9 MB (4863157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfc1bf8ce728acff89f87564fb40e67def44a450bd0e29f09309dad99e81ac6`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c52785e040cd5cb0b784f0b7cf87f4ef40f0031383deb06acd3a5018bd0eee`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:12b766cef3be0b9dc70e35a9cefcecbfad16a19e00b94a4737134ebbee24ea31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cc5ce43b7fd2c1dc34d986696c64da1a158fc067f5a4710ce475ce2f10eaec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:01:15 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:01:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:01:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:01:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:01:21 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:01:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508da0a7a8c69badd89084de30d788f3c0bc57d625677ec7d68c32f18d466ba`  
		Last Modified: Wed, 04 May 2022 22:03:28 GMT  
		Size: 4.5 MB (4510625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7965b001731ee55e0b7b2c11c7ff5f851afaed57dba5ef2a08324fab5de994f7`  
		Last Modified: Wed, 04 May 2022 22:03:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d031fa4afb68088db4a684f2332c5c8c3ecedb55d2aee461d64c8556afb468`  
		Last Modified: Wed, 04 May 2022 22:03:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:7d6c71099975b1e928511819a05612d582d412c5ed2838f04882514d0e77fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6930001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3813055a26f58efed9d97ad053203ba493589fa6e486f3dd5810354defc6b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:17:46 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:17:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:17:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:17:51 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:17:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3de3c7329a4a2fbd9e8c9cd595a837860930995c5a11d2459e045b8d2dab`  
		Last Modified: Wed, 04 May 2022 22:20:00 GMT  
		Size: 4.5 MB (4504680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc12ec06d594c70e53bb45c9912d27ad4869faf092615047ea9faab11d6ccb`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0c0af17ebf42f5af072c2b71c091af0b659ac5e20a80c92ca74da9ec5353d`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:81e20b06f2b5aac1ca438142975de9c05234b243fcb497ab8afd7f0bcd4a28a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2a5e86ad6fc84ed6f66fecfc26474466d0f61712b85aa012fc0b7e726019e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:48:24 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:48:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:48:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:48:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:48:29 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:48:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7ea9151b15b8e90d2a0ef58393de32cefb12a7f7c7e3d7a011808b38e59565`  
		Last Modified: Wed, 04 May 2022 21:49:31 GMT  
		Size: 4.5 MB (4490808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f800447a181fc7e3f37c2e68d8374347459e1d12a8d8c8653b7da45180ae97f`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f3b307d2ae2b261df9d763e886b3ae75f9aba6dc927eaf3f28cae9375c050`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-linux`

```console
$ docker pull nats@sha256:9ca8ac020e042cf31f48e19cc98dedc2f892e52a4da8b9f6db890c79a351adb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-linux` - linux; amd64

```console
$ docker pull nats@sha256:c4c5aa8d8b2ce861febd7bd4dcd9a729204ba3f15f91fd96f45ab5a6e100e516
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca6ed6836bb8a2f8705608091864ce3c25b8ca32693003e2a8df04e30dc0f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 22:19:51 GMT
COPY file:8ff89c4fbf2c06b0c443f547e21c09f4d00bc37565795d87bfb43a04d4ff236e in /nats-server 
# Mon, 23 May 2022 22:19:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 22:19:51 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 22:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:49229864ce5450b6b5291aa946e418a9b56e6bbac1179c2a3ca592284b674f6c`  
		Last Modified: Mon, 23 May 2022 22:20:42 GMT  
		Size: 4.6 MB (4589871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f11a75312c73ef42e06951cc5acd4b2690648b1ab001bacda9622a11819993`  
		Last Modified: Mon, 23 May 2022 22:20:41 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver`

```console
$ docker pull nats@sha256:f338915431c6f74ef7061f9d4349709e849edca4a9f6492c84cce0132a9219f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:95b08fc423ab3d372702336dae5a8dbe2d1da429c18eeaf36f936fc0875ee7ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107772713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5d6c0f979e88d8401fee505a489498a7f206548060dfbf92e3adf4875a8ef8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 23 May 2022 22:16:52 GMT
RUN cmd /S /C #(nop) COPY file:20c5da4e402adeb74e59df38a88afb7f0706725d1cf47a32deba2a95222bf05e in C:\nats-server.exe 
# Mon, 23 May 2022 22:16:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 23 May 2022 22:16:55 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75ab9a5e0f44e79c3adfc8b401bd352612bfa1c195e182dfedca24907fc2cb`  
		Last Modified: Mon, 23 May 2022 22:17:51 GMT  
		Size: 4.6 MB (4632778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7d580b9477c406ac03b52996e543c4d98651c583032c1cc8a15b97a42974d0`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0c44352b5c88d59e36acd76446dfd0543670ed32caba214353a395b0e27590`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430a07615e58e42c48f51d89c04072d98127ea7db787f97cdef0385b134fe681`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272f4f628d52da760d5a41b2c254fe1082dbf88591529f520cc4d37a317a47`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-nanoserver-1809`

```console
$ docker pull nats@sha256:f338915431c6f74ef7061f9d4349709e849edca4a9f6492c84cce0132a9219f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:95b08fc423ab3d372702336dae5a8dbe2d1da429c18eeaf36f936fc0875ee7ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107772713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5d6c0f979e88d8401fee505a489498a7f206548060dfbf92e3adf4875a8ef8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 23 May 2022 22:16:52 GMT
RUN cmd /S /C #(nop) COPY file:20c5da4e402adeb74e59df38a88afb7f0706725d1cf47a32deba2a95222bf05e in C:\nats-server.exe 
# Mon, 23 May 2022 22:16:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 23 May 2022 22:16:55 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75ab9a5e0f44e79c3adfc8b401bd352612bfa1c195e182dfedca24907fc2cb`  
		Last Modified: Mon, 23 May 2022 22:17:51 GMT  
		Size: 4.6 MB (4632778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7d580b9477c406ac03b52996e543c4d98651c583032c1cc8a15b97a42974d0`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0c44352b5c88d59e36acd76446dfd0543670ed32caba214353a395b0e27590`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430a07615e58e42c48f51d89c04072d98127ea7db787f97cdef0385b134fe681`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272f4f628d52da760d5a41b2c254fe1082dbf88591529f520cc4d37a317a47`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-scratch`

```console
$ docker pull nats@sha256:9ca8ac020e042cf31f48e19cc98dedc2f892e52a4da8b9f6db890c79a351adb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-scratch` - linux; amd64

```console
$ docker pull nats@sha256:c4c5aa8d8b2ce861febd7bd4dcd9a729204ba3f15f91fd96f45ab5a6e100e516
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca6ed6836bb8a2f8705608091864ce3c25b8ca32693003e2a8df04e30dc0f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 22:19:51 GMT
COPY file:8ff89c4fbf2c06b0c443f547e21c09f4d00bc37565795d87bfb43a04d4ff236e in /nats-server 
# Mon, 23 May 2022 22:19:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 22:19:51 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 22:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:49229864ce5450b6b5291aa946e418a9b56e6bbac1179c2a3ca592284b674f6c`  
		Last Modified: Mon, 23 May 2022 22:20:42 GMT  
		Size: 4.6 MB (4589871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f11a75312c73ef42e06951cc5acd4b2690648b1ab001bacda9622a11819993`  
		Last Modified: Mon, 23 May 2022 22:20:41 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore`

```console
$ docker pull nats@sha256:eb36b93a9338c371fb136c3966ea0b1d41c268eb78dcc3f0cf4b4e4e6dc2f924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:463326eba88d62c6de77af4874f4dea9ef53d30a6606dc475205c5444dd14c81
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509545826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5404ddeeb235704c9be25463973cf8749998a527098877629130155ee1a8de6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Mon, 23 May 2022 22:14:24 GMT
ENV NATS_SERVER=2.8.3
# Mon, 23 May 2022 22:14:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.3/nats-server-v2.8.3-windows-amd64.zip
# Mon, 23 May 2022 22:14:25 GMT
ENV NATS_SERVER_SHASUM=8195903f1d389327041ed50dddd62715b6aa74cc3f8f94865a8ae7b5875b3851
# Mon, 23 May 2022 22:15:24 GMT
RUN Set-PSDebug -Trace 2
# Mon, 23 May 2022 22:16:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 23 May 2022 22:16:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 23 May 2022 22:16:39 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:16:40 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 23 May 2022 22:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57b75a2edf35183ae898a9d68d8f5198163c53e5451d8da3b6a181ea8fa457f`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a0c943278e9a6934267b495e21157256a8e0e59112d219700f1569327f153`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df2fa385bec1c86f1db9e768adf0323d7ae63afc30b2b61659eb4da17fc1412`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a33a8f0bf09b30dd9167b4150806163869b35f9c43ea15769b422ef5eaa919f`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 497.4 KB (497358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf09bb112173ae8d9e2df16abe56deb21191a622f289250dbc71ecff4b8faf3`  
		Last Modified: Mon, 23 May 2022 22:17:31 GMT  
		Size: 5.0 MB (4980200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e5cc1fbe4cfbdbdeceba96cd585d66515fb4ef8e79b738fb3cff04474e6f6d`  
		Last Modified: Mon, 23 May 2022 22:17:25 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600c2585823168fbd8f9f26a1dda94da2579919da1485501b17c799a1968a86c`  
		Last Modified: Mon, 23 May 2022 22:17:26 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3960c981235519da3181138ec9e48ef481177d8129cccc3620327e71a7c29860`  
		Last Modified: Mon, 23 May 2022 22:17:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c546fa758ac26156e07083b8d1919a68568872dace58969c4714577dddfc1a3`  
		Last Modified: Mon, 23 May 2022 22:17:25 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2-windowsservercore-1809`

```console
$ docker pull nats@sha256:eb36b93a9338c371fb136c3966ea0b1d41c268eb78dcc3f0cf4b4e4e6dc2f924
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:463326eba88d62c6de77af4874f4dea9ef53d30a6606dc475205c5444dd14c81
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509545826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5404ddeeb235704c9be25463973cf8749998a527098877629130155ee1a8de6`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Mon, 23 May 2022 22:14:24 GMT
ENV NATS_SERVER=2.8.3
# Mon, 23 May 2022 22:14:24 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.3/nats-server-v2.8.3-windows-amd64.zip
# Mon, 23 May 2022 22:14:25 GMT
ENV NATS_SERVER_SHASUM=8195903f1d389327041ed50dddd62715b6aa74cc3f8f94865a8ae7b5875b3851
# Mon, 23 May 2022 22:15:24 GMT
RUN Set-PSDebug -Trace 2
# Mon, 23 May 2022 22:16:37 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Mon, 23 May 2022 22:16:38 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 23 May 2022 22:16:39 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:16:40 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 23 May 2022 22:16:41 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f57b75a2edf35183ae898a9d68d8f5198163c53e5451d8da3b6a181ea8fa457f`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44a0c943278e9a6934267b495e21157256a8e0e59112d219700f1569327f153`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1df2fa385bec1c86f1db9e768adf0323d7ae63afc30b2b61659eb4da17fc1412`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a33a8f0bf09b30dd9167b4150806163869b35f9c43ea15769b422ef5eaa919f`  
		Last Modified: Mon, 23 May 2022 22:17:28 GMT  
		Size: 497.4 KB (497358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf09bb112173ae8d9e2df16abe56deb21191a622f289250dbc71ecff4b8faf3`  
		Last Modified: Mon, 23 May 2022 22:17:31 GMT  
		Size: 5.0 MB (4980200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0e5cc1fbe4cfbdbdeceba96cd585d66515fb4ef8e79b738fb3cff04474e6f6d`  
		Last Modified: Mon, 23 May 2022 22:17:25 GMT  
		Size: 1.8 KB (1846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600c2585823168fbd8f9f26a1dda94da2579919da1485501b17c799a1968a86c`  
		Last Modified: Mon, 23 May 2022 22:17:26 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3960c981235519da3181138ec9e48ef481177d8129cccc3620327e71a7c29860`  
		Last Modified: Mon, 23 May 2022 22:17:25 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c546fa758ac26156e07083b8d1919a68568872dace58969c4714577dddfc1a3`  
		Last Modified: Mon, 23 May 2022 22:17:25 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8`

```console
$ docker pull nats@sha256:c140d3e0949999f528dd57e016c34ee4916ede78f38a75a8c6f9c294f6d109ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8` - linux; amd64

```console
$ docker pull nats@sha256:c4c5aa8d8b2ce861febd7bd4dcd9a729204ba3f15f91fd96f45ab5a6e100e516
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca6ed6836bb8a2f8705608091864ce3c25b8ca32693003e2a8df04e30dc0f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 22:19:51 GMT
COPY file:8ff89c4fbf2c06b0c443f547e21c09f4d00bc37565795d87bfb43a04d4ff236e in /nats-server 
# Mon, 23 May 2022 22:19:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 22:19:51 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 22:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:49229864ce5450b6b5291aa946e418a9b56e6bbac1179c2a3ca592284b674f6c`  
		Last Modified: Mon, 23 May 2022 22:20:42 GMT  
		Size: 4.6 MB (4589871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f11a75312c73ef42e06951cc5acd4b2690648b1ab001bacda9622a11819993`  
		Last Modified: Mon, 23 May 2022 22:20:41 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:95b08fc423ab3d372702336dae5a8dbe2d1da429c18eeaf36f936fc0875ee7ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107772713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5d6c0f979e88d8401fee505a489498a7f206548060dfbf92e3adf4875a8ef8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 23 May 2022 22:16:52 GMT
RUN cmd /S /C #(nop) COPY file:20c5da4e402adeb74e59df38a88afb7f0706725d1cf47a32deba2a95222bf05e in C:\nats-server.exe 
# Mon, 23 May 2022 22:16:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 23 May 2022 22:16:55 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75ab9a5e0f44e79c3adfc8b401bd352612bfa1c195e182dfedca24907fc2cb`  
		Last Modified: Mon, 23 May 2022 22:17:51 GMT  
		Size: 4.6 MB (4632778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7d580b9477c406ac03b52996e543c4d98651c583032c1cc8a15b97a42974d0`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0c44352b5c88d59e36acd76446dfd0543670ed32caba214353a395b0e27590`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430a07615e58e42c48f51d89c04072d98127ea7db787f97cdef0385b134fe681`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272f4f628d52da760d5a41b2c254fe1082dbf88591529f520cc4d37a317a47`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-alpine`

```console
$ docker pull nats@sha256:6ce50789c72aee8684c30383c8b49b80613cec2b81c61ed17f446a770fe6c705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-alpine` - linux; amd64

```console
$ docker pull nats@sha256:2769de3270a9a86a1f799007cb1be2cbac229c07395206d13fbf845312481fc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0303f1d0cccc66a96da1353b9732b2b1b9dbd21206996b9af197b108e52d444b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Mon, 23 May 2022 22:19:43 GMT
ENV NATS_SERVER=2.8.3
# Mon, 23 May 2022 22:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='905df5647dba0443ce6b92116ff5c6ceb49d3e24fa78c999d0c19fe634f341d6' ;; 		armhf) natsArch='arm6'; sha256='590a0460362ab1fc47ebce8886f5a53ff8b91abefa412ce77762f8514041394b' ;; 		armv7) natsArch='arm7'; sha256='142673f4eafca832e0347b1be0f5f9b0b7b23a46c08a623b63c6925a94a2d9f1' ;; 		x86_64) natsArch='amd64'; sha256='16e6bfa14e8ba9bc7d924e296bfe6bcad803b04318e6d60ef14ee45e3d3ddc60' ;; 		x86) natsArch='386'; sha256='fc749ab7574aa9ae22661a89ad73ac26331772e2302197d1625db56e967a74ac' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 23 May 2022 22:19:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 23 May 2022 22:19:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 23 May 2022 22:19:45 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 22:19:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68886d04807b30a327d175e97fe6fa560a6f4e68ea614397e87e7d456d6ace19`  
		Last Modified: Mon, 23 May 2022 22:20:18 GMT  
		Size: 4.9 MB (4863157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfc1bf8ce728acff89f87564fb40e67def44a450bd0e29f09309dad99e81ac6`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c52785e040cd5cb0b784f0b7cf87f4ef40f0031383deb06acd3a5018bd0eee`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:12b766cef3be0b9dc70e35a9cefcecbfad16a19e00b94a4737134ebbee24ea31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cc5ce43b7fd2c1dc34d986696c64da1a158fc067f5a4710ce475ce2f10eaec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:01:15 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:01:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:01:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:01:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:01:21 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:01:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508da0a7a8c69badd89084de30d788f3c0bc57d625677ec7d68c32f18d466ba`  
		Last Modified: Wed, 04 May 2022 22:03:28 GMT  
		Size: 4.5 MB (4510625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7965b001731ee55e0b7b2c11c7ff5f851afaed57dba5ef2a08324fab5de994f7`  
		Last Modified: Wed, 04 May 2022 22:03:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d031fa4afb68088db4a684f2332c5c8c3ecedb55d2aee461d64c8556afb468`  
		Last Modified: Wed, 04 May 2022 22:03:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7d6c71099975b1e928511819a05612d582d412c5ed2838f04882514d0e77fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6930001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3813055a26f58efed9d97ad053203ba493589fa6e486f3dd5810354defc6b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:17:46 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:17:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:17:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:17:51 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:17:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3de3c7329a4a2fbd9e8c9cd595a837860930995c5a11d2459e045b8d2dab`  
		Last Modified: Wed, 04 May 2022 22:20:00 GMT  
		Size: 4.5 MB (4504680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc12ec06d594c70e53bb45c9912d27ad4869faf092615047ea9faab11d6ccb`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0c0af17ebf42f5af072c2b71c091af0b659ac5e20a80c92ca74da9ec5353d`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:81e20b06f2b5aac1ca438142975de9c05234b243fcb497ab8afd7f0bcd4a28a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2a5e86ad6fc84ed6f66fecfc26474466d0f61712b85aa012fc0b7e726019e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:48:24 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:48:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:48:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:48:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:48:29 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:48:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7ea9151b15b8e90d2a0ef58393de32cefb12a7f7c7e3d7a011808b38e59565`  
		Last Modified: Wed, 04 May 2022 21:49:31 GMT  
		Size: 4.5 MB (4490808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f800447a181fc7e3f37c2e68d8374347459e1d12a8d8c8653b7da45180ae97f`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f3b307d2ae2b261df9d763e886b3ae75f9aba6dc927eaf3f28cae9375c050`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-alpine3.15`

```console
$ docker pull nats@sha256:6ce50789c72aee8684c30383c8b49b80613cec2b81c61ed17f446a770fe6c705
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:2769de3270a9a86a1f799007cb1be2cbac229c07395206d13fbf845312481fc8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7678717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0303f1d0cccc66a96da1353b9732b2b1b9dbd21206996b9af197b108e52d444b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Mon, 23 May 2022 22:19:43 GMT
ENV NATS_SERVER=2.8.3
# Mon, 23 May 2022 22:19:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='905df5647dba0443ce6b92116ff5c6ceb49d3e24fa78c999d0c19fe634f341d6' ;; 		armhf) natsArch='arm6'; sha256='590a0460362ab1fc47ebce8886f5a53ff8b91abefa412ce77762f8514041394b' ;; 		armv7) natsArch='arm7'; sha256='142673f4eafca832e0347b1be0f5f9b0b7b23a46c08a623b63c6925a94a2d9f1' ;; 		x86_64) natsArch='amd64'; sha256='16e6bfa14e8ba9bc7d924e296bfe6bcad803b04318e6d60ef14ee45e3d3ddc60' ;; 		x86) natsArch='386'; sha256='fc749ab7574aa9ae22661a89ad73ac26331772e2302197d1625db56e967a74ac' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 23 May 2022 22:19:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 23 May 2022 22:19:45 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 23 May 2022 22:19:45 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 22:19:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68886d04807b30a327d175e97fe6fa560a6f4e68ea614397e87e7d456d6ace19`  
		Last Modified: Mon, 23 May 2022 22:20:18 GMT  
		Size: 4.9 MB (4863157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebfc1bf8ce728acff89f87564fb40e67def44a450bd0e29f09309dad99e81ac6`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49c52785e040cd5cb0b784f0b7cf87f4ef40f0031383deb06acd3a5018bd0eee`  
		Last Modified: Mon, 23 May 2022 22:20:17 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:12b766cef3be0b9dc70e35a9cefcecbfad16a19e00b94a4737134ebbee24ea31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cc5ce43b7fd2c1dc34d986696c64da1a158fc067f5a4710ce475ce2f10eaec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:01:15 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:01:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:01:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:01:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:01:21 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:01:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508da0a7a8c69badd89084de30d788f3c0bc57d625677ec7d68c32f18d466ba`  
		Last Modified: Wed, 04 May 2022 22:03:28 GMT  
		Size: 4.5 MB (4510625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7965b001731ee55e0b7b2c11c7ff5f851afaed57dba5ef2a08324fab5de994f7`  
		Last Modified: Wed, 04 May 2022 22:03:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d031fa4afb68088db4a684f2332c5c8c3ecedb55d2aee461d64c8556afb468`  
		Last Modified: Wed, 04 May 2022 22:03:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:7d6c71099975b1e928511819a05612d582d412c5ed2838f04882514d0e77fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6930001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3813055a26f58efed9d97ad053203ba493589fa6e486f3dd5810354defc6b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:17:46 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:17:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:17:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:17:51 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:17:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3de3c7329a4a2fbd9e8c9cd595a837860930995c5a11d2459e045b8d2dab`  
		Last Modified: Wed, 04 May 2022 22:20:00 GMT  
		Size: 4.5 MB (4504680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc12ec06d594c70e53bb45c9912d27ad4869faf092615047ea9faab11d6ccb`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0c0af17ebf42f5af072c2b71c091af0b659ac5e20a80c92ca74da9ec5353d`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:81e20b06f2b5aac1ca438142975de9c05234b243fcb497ab8afd7f0bcd4a28a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2a5e86ad6fc84ed6f66fecfc26474466d0f61712b85aa012fc0b7e726019e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:48:24 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:48:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:48:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:48:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:48:29 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:48:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7ea9151b15b8e90d2a0ef58393de32cefb12a7f7c7e3d7a011808b38e59565`  
		Last Modified: Wed, 04 May 2022 21:49:31 GMT  
		Size: 4.5 MB (4490808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f800447a181fc7e3f37c2e68d8374347459e1d12a8d8c8653b7da45180ae97f`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f3b307d2ae2b261df9d763e886b3ae75f9aba6dc927eaf3f28cae9375c050`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-linux`

```console
$ docker pull nats@sha256:9ca8ac020e042cf31f48e19cc98dedc2f892e52a4da8b9f6db890c79a351adb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-linux` - linux; amd64

```console
$ docker pull nats@sha256:c4c5aa8d8b2ce861febd7bd4dcd9a729204ba3f15f91fd96f45ab5a6e100e516
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4590377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ca6ed6836bb8a2f8705608091864ce3c25b8ca32693003e2a8df04e30dc0f9`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Mon, 23 May 2022 22:19:51 GMT
COPY file:8ff89c4fbf2c06b0c443f547e21c09f4d00bc37565795d87bfb43a04d4ff236e in /nats-server 
# Mon, 23 May 2022 22:19:51 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Mon, 23 May 2022 22:19:51 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:19:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Mon, 23 May 2022 22:19:52 GMT
ENTRYPOINT ["/nats-server"]
# Mon, 23 May 2022 22:19:52 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:49229864ce5450b6b5291aa946e418a9b56e6bbac1179c2a3ca592284b674f6c`  
		Last Modified: Mon, 23 May 2022 22:20:42 GMT  
		Size: 4.6 MB (4589871 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f11a75312c73ef42e06951cc5acd4b2690648b1ab001bacda9622a11819993`  
		Last Modified: Mon, 23 May 2022 22:20:41 GMT  
		Size: 506.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-nanoserver`

```console
$ docker pull nats@sha256:f338915431c6f74ef7061f9d4349709e849edca4a9f6492c84cce0132a9219f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:95b08fc423ab3d372702336dae5a8dbe2d1da429c18eeaf36f936fc0875ee7ac
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107772713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd5d6c0f979e88d8401fee505a489498a7f206548060dfbf92e3adf4875a8ef8`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Mon, 23 May 2022 22:16:52 GMT
RUN cmd /S /C #(nop) COPY file:20c5da4e402adeb74e59df38a88afb7f0706725d1cf47a32deba2a95222bf05e in C:\nats-server.exe 
# Mon, 23 May 2022 22:16:53 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Mon, 23 May 2022 22:16:54 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Mon, 23 May 2022 22:16:55 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c75ab9a5e0f44e79c3adfc8b401bd352612bfa1c195e182dfedca24907fc2cb`  
		Last Modified: Mon, 23 May 2022 22:17:51 GMT  
		Size: 4.6 MB (4632778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e7d580b9477c406ac03b52996e543c4d98651c583032c1cc8a15b97a42974d0`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.7 KB (1660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f0c44352b5c88d59e36acd76446dfd0543670ed32caba214353a395b0e27590`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430a07615e58e42c48f51d89c04072d98127ea7db787f97cdef0385b134fe681`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51272f4f628d52da760d5a41b2c254fe1082dbf88591529f520cc4d37a317a47`  
		Last Modified: Mon, 23 May 2022 22:17:46 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-nanoserver-1809`

```console
$ docker pull nats@sha256:a778e8e1e3203b35fe0bdb6c5a94e8f63de63b9f4bf2eaf17eee3317170649c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:f91885fa620a9738072e61f4d68d9a8400803e2cfafda40886de5903451520e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2bd603b8bbf94bbdf8466e6848b146754fe29271b8e95884a8d2abcfac67eb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:42:08 GMT
RUN cmd /S /C #(nop) COPY file:1e690007468fe11473f18dc8fbc8b7aa29351e71d03ca73f75d9fcfbf1fd7911 in C:\nats-server.exe 
# Wed, 11 May 2022 14:42:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5fb401df1c150a43c2ec9b3ff57a672b92c67107234ab008625c5fea9f9e69`  
		Last Modified: Wed, 11 May 2022 14:43:04 GMT  
		Size: 4.6 MB (4622748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09ac197c7dae98dd6fa2697e81011965729a49252e223601d418ba0ad439c36`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f37eaf04793dd48de8ebbf4bd5188e4d0f528f5047265be5c86a5d12c133c26`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae6fc61c5a618a623aef25b66fda889d02d4ca7084477f4c21831a7150291d`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e7ab8b701dbc07245b31e34f1ed8493639f5d99ae276a089bd8c7a35a8bca9`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-scratch`

```console
$ docker pull nats@sha256:dd400785e2c069158ca6a488873976cab93098904db7fcc044cfc6af0327640c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2.8-scratch` - linux; amd64

```console
$ docker pull nats@sha256:d7022e467f53812285667fd004413e8cb15920efbb01d1d0f7c4194a2e084959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71863590dea616f7cf93b753e1e7a3baf16f89747f06004d08f65d3fa907ee9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:19:54 GMT
COPY file:1b0e004de765c2bffa3154a8b1990e8a621636f4f1d7ff504c566b8ba440d227 in /nats-server 
# Wed, 04 May 2022 21:19:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:19:54 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:19:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:19:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cf7d6008a72749fed702f25d8a1bb63636b75bf34655ba074286dc54d0db2b5b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 4.6 MB (4579600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ef91ad4507cb0bd768e027792377ba07aaaebc8d89981a6ee648d58561273b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2.8-scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-windowsservercore`

```console
$ docker pull nats@sha256:07432a398099039390dadc22e657dfbc8ada5a6475071cdf3a0e7ae97cc5f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:4c410fa02ac3030e41f939d40f93ef6f4b8fa5ef0018742f84ded81ff3dd56f4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509506739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310f6ed1347d5414cbccdf037d24ac72f6a164094e11c88c95c36add4ca70e7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:39:54 GMT
ENV NATS_SERVER=2.8.2
# Wed, 11 May 2022 14:39:55 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.2/nats-server-v2.8.2-windows-amd64.zip
# Wed, 11 May 2022 14:39:56 GMT
ENV NATS_SERVER_SHASUM=300b9743afa50e02e4e8d43dc212bfde8a871617bd524829114e19ff680dde11
# Wed, 11 May 2022 14:40:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 14:41:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 14:41:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:41:58 GMT
EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:41:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705248b3431d43594f02c1a498c5825693a2219dc3e9916401f0c6483917d9a`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb084aa44aefde2d0aa2b439015601202b9289be01b36d72c372e12b207c0e3`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c26ed0b144ad0936998810c48866b8542c5459336cfbc516abbd8e36f335dc`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be12ae5206975ef6a801832e7cb1e13cce3a20a913b8af575d2eb06033f814b`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 482.2 KB (482237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934d847ec8d58fee43acc3f6b9da54c22bbaa3af2fdc22fc6cc7b544df9ed0d`  
		Last Modified: Wed, 11 May 2022 14:42:41 GMT  
		Size: 5.0 MB (4955482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b1d767c6565af1eb4447e5b0ce9d14889a68e438a8f16385c402174fe0d560`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7197706e722c8737fffdee9b04e1f3d7e8e6bc8824673d7f30221ee05c25681`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc51eeff832289639769559e0535687ae4a579b49d847a4fb7236824a8805`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925945a5e74fac0f93b1337cf5af3f61b3b33e549af73c3b2ff6effa8cbe27e4`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8-windowsservercore-1809`

```console
$ docker pull nats@sha256:07432a398099039390dadc22e657dfbc8ada5a6475071cdf3a0e7ae97cc5f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:2.8-windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:4c410fa02ac3030e41f939d40f93ef6f4b8fa5ef0018742f84ded81ff3dd56f4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509506739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310f6ed1347d5414cbccdf037d24ac72f6a164094e11c88c95c36add4ca70e7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:39:54 GMT
ENV NATS_SERVER=2.8.2
# Wed, 11 May 2022 14:39:55 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.2/nats-server-v2.8.2-windows-amd64.zip
# Wed, 11 May 2022 14:39:56 GMT
ENV NATS_SERVER_SHASUM=300b9743afa50e02e4e8d43dc212bfde8a871617bd524829114e19ff680dde11
# Wed, 11 May 2022 14:40:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 14:41:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 14:41:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:41:58 GMT
EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:41:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705248b3431d43594f02c1a498c5825693a2219dc3e9916401f0c6483917d9a`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb084aa44aefde2d0aa2b439015601202b9289be01b36d72c372e12b207c0e3`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c26ed0b144ad0936998810c48866b8542c5459336cfbc516abbd8e36f335dc`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be12ae5206975ef6a801832e7cb1e13cce3a20a913b8af575d2eb06033f814b`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 482.2 KB (482237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934d847ec8d58fee43acc3f6b9da54c22bbaa3af2fdc22fc6cc7b544df9ed0d`  
		Last Modified: Wed, 11 May 2022 14:42:41 GMT  
		Size: 5.0 MB (4955482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b1d767c6565af1eb4447e5b0ce9d14889a68e438a8f16385c402174fe0d560`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7197706e722c8737fffdee9b04e1f3d7e8e6bc8824673d7f30221ee05c25681`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc51eeff832289639769559e0535687ae4a579b49d847a4fb7236824a8805`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925945a5e74fac0f93b1337cf5af3f61b3b33e549af73c3b2ff6effa8cbe27e4`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:2.8.3`

**does not exist** (yet?)

## `nats:2.8.3-alpine`

**does not exist** (yet?)

## `nats:2.8.3-alpine3.15`

**does not exist** (yet?)

## `nats:2.8.3-linux`

**does not exist** (yet?)

## `nats:2.8.3-nanoserver`

**does not exist** (yet?)

## `nats:2.8.3-nanoserver-1809`

**does not exist** (yet?)

## `nats:2.8.3-scratch`

**does not exist** (yet?)

## `nats:2.8.3-windowsservercore`

**does not exist** (yet?)

## `nats:2.8.3-windowsservercore-1809`

**does not exist** (yet?)

## `nats:alpine`

```console
$ docker pull nats@sha256:51ed1dcadcd928cbca6b4b2846491bd14667dca111ac63fdb001eef89cb9192f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:3dfa6b8def0d3c784ef7827f0c21b17afd01be56773c68d5950e9f29172ae796
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7667828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3370f8d5fa5f0ea4cfdcaa60d7f568c2cf9e9752f3a75d11b0d30a257db8a51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:19:44 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:19:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:19:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:19:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:19:47 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:19:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb157527e1f2e860f2700cadfdf0bed3ac0d50b8a177dd0b906431b0d46b44b5`  
		Last Modified: Wed, 04 May 2022 21:20:20 GMT  
		Size: 4.9 MB (4852271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29bade32b2ef2ecc8325cbc5cbbf69470e5e20cc04e292244e704f68b9a6f86`  
		Last Modified: Wed, 04 May 2022 21:20:19 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbec41bc3a042cdbf4c2e9b57c99bf99a4552e64a437be0066d42a04e3de650`  
		Last Modified: Wed, 04 May 2022 21:20:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:12b766cef3be0b9dc70e35a9cefcecbfad16a19e00b94a4737134ebbee24ea31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cc5ce43b7fd2c1dc34d986696c64da1a158fc067f5a4710ce475ce2f10eaec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:01:15 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:01:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:01:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:01:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:01:21 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:01:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508da0a7a8c69badd89084de30d788f3c0bc57d625677ec7d68c32f18d466ba`  
		Last Modified: Wed, 04 May 2022 22:03:28 GMT  
		Size: 4.5 MB (4510625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7965b001731ee55e0b7b2c11c7ff5f851afaed57dba5ef2a08324fab5de994f7`  
		Last Modified: Wed, 04 May 2022 22:03:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d031fa4afb68088db4a684f2332c5c8c3ecedb55d2aee461d64c8556afb468`  
		Last Modified: Wed, 04 May 2022 22:03:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:7d6c71099975b1e928511819a05612d582d412c5ed2838f04882514d0e77fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6930001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3813055a26f58efed9d97ad053203ba493589fa6e486f3dd5810354defc6b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:17:46 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:17:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:17:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:17:51 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:17:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3de3c7329a4a2fbd9e8c9cd595a837860930995c5a11d2459e045b8d2dab`  
		Last Modified: Wed, 04 May 2022 22:20:00 GMT  
		Size: 4.5 MB (4504680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc12ec06d594c70e53bb45c9912d27ad4869faf092615047ea9faab11d6ccb`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0c0af17ebf42f5af072c2b71c091af0b659ac5e20a80c92ca74da9ec5353d`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:81e20b06f2b5aac1ca438142975de9c05234b243fcb497ab8afd7f0bcd4a28a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2a5e86ad6fc84ed6f66fecfc26474466d0f61712b85aa012fc0b7e726019e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:48:24 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:48:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:48:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:48:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:48:29 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:48:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7ea9151b15b8e90d2a0ef58393de32cefb12a7f7c7e3d7a011808b38e59565`  
		Last Modified: Wed, 04 May 2022 21:49:31 GMT  
		Size: 4.5 MB (4490808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f800447a181fc7e3f37c2e68d8374347459e1d12a8d8c8653b7da45180ae97f`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f3b307d2ae2b261df9d763e886b3ae75f9aba6dc927eaf3f28cae9375c050`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:alpine3.15`

```console
$ docker pull nats@sha256:51ed1dcadcd928cbca6b4b2846491bd14667dca111ac63fdb001eef89cb9192f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

```console
$ docker pull nats@sha256:3dfa6b8def0d3c784ef7827f0c21b17afd01be56773c68d5950e9f29172ae796
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7667828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3370f8d5fa5f0ea4cfdcaa60d7f568c2cf9e9752f3a75d11b0d30a257db8a51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 05 Apr 2022 00:19:59 GMT
ADD file:5d673d25da3a14ce1f6cf66e4c7fd4f4b85a3759a9d93efb3fd9ff852b5b56e4 in / 
# Tue, 05 Apr 2022 00:19:59 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:19:44 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:19:47 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:19:47 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:19:47 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:19:47 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:19:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:df9b9388f04ad6279a7410b85cedfdcb2208c0a003da7ab5613af71079148139`  
		Last Modified: Mon, 04 Apr 2022 19:10:16 GMT  
		Size: 2.8 MB (2814559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb157527e1f2e860f2700cadfdf0bed3ac0d50b8a177dd0b906431b0d46b44b5`  
		Last Modified: Wed, 04 May 2022 21:20:20 GMT  
		Size: 4.9 MB (4852271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29bade32b2ef2ecc8325cbc5cbbf69470e5e20cc04e292244e704f68b9a6f86`  
		Last Modified: Wed, 04 May 2022 21:20:19 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dbec41bc3a042cdbf4c2e9b57c99bf99a4552e64a437be0066d42a04e3de650`  
		Last Modified: Wed, 04 May 2022 21:20:19 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:12b766cef3be0b9dc70e35a9cefcecbfad16a19e00b94a4737134ebbee24ea31
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7133599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cc5ce43b7fd2c1dc34d986696c64da1a158fc067f5a4710ce475ce2f10eaec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:01:15 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:01:19 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:01:20 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:01:20 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:01:21 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:01:21 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3508da0a7a8c69badd89084de30d788f3c0bc57d625677ec7d68c32f18d466ba`  
		Last Modified: Wed, 04 May 2022 22:03:28 GMT  
		Size: 4.5 MB (4510625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7965b001731ee55e0b7b2c11c7ff5f851afaed57dba5ef2a08324fab5de994f7`  
		Last Modified: Wed, 04 May 2022 22:03:27 GMT  
		Size: 587.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d031fa4afb68088db4a684f2332c5c8c3ecedb55d2aee461d64c8556afb468`  
		Last Modified: Wed, 04 May 2022 22:03:25 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:7d6c71099975b1e928511819a05612d582d412c5ed2838f04882514d0e77fff8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6930001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3813055a26f58efed9d97ad053203ba493589fa6e486f3dd5810354defc6b3c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 22:17:46 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 22:17:50 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 22:17:50 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 22:17:51 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 22:17:51 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:17:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 22:17:52 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49f3de3c7329a4a2fbd9e8c9cd595a837860930995c5a11d2459e045b8d2dab`  
		Last Modified: Wed, 04 May 2022 22:20:00 GMT  
		Size: 4.5 MB (4504680 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51dc12ec06d594c70e53bb45c9912d27ad4869faf092615047ea9faab11d6ccb`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 584.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e0c0af17ebf42f5af072c2b71c091af0b659ac5e20a80c92ca74da9ec5353d`  
		Last Modified: Wed, 04 May 2022 22:19:57 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:81e20b06f2b5aac1ca438142975de9c05234b243fcb497ab8afd7f0bcd4a28a8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7208259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12c2a5e86ad6fc84ed6f66fecfc26474466d0f61712b85aa012fc0b7e726019e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Wed, 04 May 2022 21:48:24 GMT
ENV NATS_SERVER=2.8.2
# Wed, 04 May 2022 21:48:26 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='3409b9dc76c0136cecded67115521d3a815f7a2f3739e81eb87a8d5d761843c3' ;; 		armhf) natsArch='arm6'; sha256='a3d474a583ca90e3577aa470335c582d4565918f500ebd28d760643fb631d8d5' ;; 		armv7) natsArch='arm7'; sha256='88fd437f7def8dbe68b17dce703c919771e64b570856bf0e6f2eb3b9459031c6' ;; 		x86_64) natsArch='amd64'; sha256='59805a464237801574ca7efdc69ebc21040e9b811fb53ed444c4808a05440719' ;; 		x86) natsArch='386'; sha256='facd3c69ee27c3e9e8654e5de95eb79de2e873bf4c066317aa9fad5c2ea26b92' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Wed, 04 May 2022 21:48:28 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Wed, 04 May 2022 21:48:29 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 04 May 2022 21:48:29 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 04 May 2022 21:48:31 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7ea9151b15b8e90d2a0ef58393de32cefb12a7f7c7e3d7a011808b38e59565`  
		Last Modified: Wed, 04 May 2022 21:49:31 GMT  
		Size: 4.5 MB (4490808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f800447a181fc7e3f37c2e68d8374347459e1d12a8d8c8653b7da45180ae97f`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894f3b307d2ae2b261df9d763e886b3ae75f9aba6dc927eaf3f28cae9375c050`  
		Last Modified: Wed, 04 May 2022 21:49:30 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:latest`

```console
$ docker pull nats@sha256:976199f47bab8358e55e7ba69b168fa5ef9d74aaca26bc5bed1e0f491069b1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	windows version 10.0.17763.2928; amd64

### `nats:latest` - linux; amd64

```console
$ docker pull nats@sha256:d7022e467f53812285667fd004413e8cb15920efbb01d1d0f7c4194a2e084959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71863590dea616f7cf93b753e1e7a3baf16f89747f06004d08f65d3fa907ee9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:19:54 GMT
COPY file:1b0e004de765c2bffa3154a8b1990e8a621636f4f1d7ff504c566b8ba440d227 in /nats-server 
# Wed, 04 May 2022 21:19:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:19:54 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:19:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:19:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cf7d6008a72749fed702f25d8a1bb63636b75bf34655ba074286dc54d0db2b5b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 4.6 MB (4579600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ef91ad4507cb0bd768e027792377ba07aaaebc8d89981a6ee648d58561273b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:latest` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:f91885fa620a9738072e61f4d68d9a8400803e2cfafda40886de5903451520e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2bd603b8bbf94bbdf8466e6848b146754fe29271b8e95884a8d2abcfac67eb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:42:08 GMT
RUN cmd /S /C #(nop) COPY file:1e690007468fe11473f18dc8fbc8b7aa29351e71d03ca73f75d9fcfbf1fd7911 in C:\nats-server.exe 
# Wed, 11 May 2022 14:42:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5fb401df1c150a43c2ec9b3ff57a672b92c67107234ab008625c5fea9f9e69`  
		Last Modified: Wed, 11 May 2022 14:43:04 GMT  
		Size: 4.6 MB (4622748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09ac197c7dae98dd6fa2697e81011965729a49252e223601d418ba0ad439c36`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f37eaf04793dd48de8ebbf4bd5188e4d0f528f5047265be5c86a5d12c133c26`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae6fc61c5a618a623aef25b66fda889d02d4ca7084477f4c21831a7150291d`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e7ab8b701dbc07245b31e34f1ed8493639f5d99ae276a089bd8c7a35a8bca9`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:linux`

```console
$ docker pull nats@sha256:dd400785e2c069158ca6a488873976cab93098904db7fcc044cfc6af0327640c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:linux` - linux; amd64

```console
$ docker pull nats@sha256:d7022e467f53812285667fd004413e8cb15920efbb01d1d0f7c4194a2e084959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71863590dea616f7cf93b753e1e7a3baf16f89747f06004d08f65d3fa907ee9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:19:54 GMT
COPY file:1b0e004de765c2bffa3154a8b1990e8a621636f4f1d7ff504c566b8ba440d227 in /nats-server 
# Wed, 04 May 2022 21:19:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:19:54 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:19:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:19:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cf7d6008a72749fed702f25d8a1bb63636b75bf34655ba074286dc54d0db2b5b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 4.6 MB (4579600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ef91ad4507cb0bd768e027792377ba07aaaebc8d89981a6ee648d58561273b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:linux` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver`

```console
$ docker pull nats@sha256:a778e8e1e3203b35fe0bdb6c5a94e8f63de63b9f4bf2eaf17eee3317170649c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:nanoserver` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:f91885fa620a9738072e61f4d68d9a8400803e2cfafda40886de5903451520e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2bd603b8bbf94bbdf8466e6848b146754fe29271b8e95884a8d2abcfac67eb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:42:08 GMT
RUN cmd /S /C #(nop) COPY file:1e690007468fe11473f18dc8fbc8b7aa29351e71d03ca73f75d9fcfbf1fd7911 in C:\nats-server.exe 
# Wed, 11 May 2022 14:42:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5fb401df1c150a43c2ec9b3ff57a672b92c67107234ab008625c5fea9f9e69`  
		Last Modified: Wed, 11 May 2022 14:43:04 GMT  
		Size: 4.6 MB (4622748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09ac197c7dae98dd6fa2697e81011965729a49252e223601d418ba0ad439c36`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f37eaf04793dd48de8ebbf4bd5188e4d0f528f5047265be5c86a5d12c133c26`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae6fc61c5a618a623aef25b66fda889d02d4ca7084477f4c21831a7150291d`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e7ab8b701dbc07245b31e34f1ed8493639f5d99ae276a089bd8c7a35a8bca9`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:nanoserver-1809`

```console
$ docker pull nats@sha256:a778e8e1e3203b35fe0bdb6c5a94e8f63de63b9f4bf2eaf17eee3317170649c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:nanoserver-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:f91885fa620a9738072e61f4d68d9a8400803e2cfafda40886de5903451520e2
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **107.8 MB (107763060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f2bd603b8bbf94bbdf8466e6848b146754fe29271b8e95884a8d2abcfac67eb`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Thu, 05 May 2022 16:42:43 GMT
RUN Apply image 10.0.17763.2928
# Wed, 11 May 2022 14:42:07 GMT
RUN cmd /S /C #(nop)  ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:42:08 GMT
RUN cmd /S /C #(nop) COPY file:1e690007468fe11473f18dc8fbc8b7aa29351e71d03ca73f75d9fcfbf1fd7911 in C:\nats-server.exe 
# Wed, 11 May 2022 14:42:09 GMT
RUN cmd /S /C #(nop) COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:42:10 GMT
RUN cmd /S /C #(nop)  ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:11 GMT
RUN cmd /S /C #(nop)  CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:6626f490e738e10ea5e31ff2643e3a8c372e076d9030c77fac37537dbf12b73c`  
		Size: 103.1 MB (103133833 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:2df39ac96d0b0efa546f2a05d81fb2a68ff8b0541fca6761bc2cedd28ff57f25`  
		Last Modified: Wed, 11 May 2022 14:43:01 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d5fb401df1c150a43c2ec9b3ff57a672b92c67107234ab008625c5fea9f9e69`  
		Last Modified: Wed, 11 May 2022 14:43:04 GMT  
		Size: 4.6 MB (4622748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f09ac197c7dae98dd6fa2697e81011965729a49252e223601d418ba0ad439c36`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.8 KB (1803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f37eaf04793dd48de8ebbf4bd5188e4d0f528f5047265be5c86a5d12c133c26`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31ae6fc61c5a618a623aef25b66fda889d02d4ca7084477f4c21831a7150291d`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e7ab8b701dbc07245b31e34f1ed8493639f5d99ae276a089bd8c7a35a8bca9`  
		Last Modified: Wed, 11 May 2022 14:42:59 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:scratch`

```console
$ docker pull nats@sha256:dd400785e2c069158ca6a488873976cab93098904db7fcc044cfc6af0327640c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:scratch` - linux; amd64

```console
$ docker pull nats@sha256:d7022e467f53812285667fd004413e8cb15920efbb01d1d0f7c4194a2e084959
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4580109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71863590dea616f7cf93b753e1e7a3baf16f89747f06004d08f65d3fa907ee9a`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:19:54 GMT
COPY file:1b0e004de765c2bffa3154a8b1990e8a621636f4f1d7ff504c566b8ba440d227 in /nats-server 
# Wed, 04 May 2022 21:19:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:19:54 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:19:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:19:54 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:19:54 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:cf7d6008a72749fed702f25d8a1bb63636b75bf34655ba074286dc54d0db2b5b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 4.6 MB (4579600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3ef91ad4507cb0bd768e027792377ba07aaaebc8d89981a6ee648d58561273b`  
		Last Modified: Wed, 04 May 2022 21:20:43 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v6

```console
$ docker pull nats@sha256:80a268344378d95bf616b13ab6e787e5a242cadbaa9c933e6708bb8761cab22f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4238279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53b2041383be620a877c3c265658998b4c5a2f31c6f26d3dd2aa53cb78cf527`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:01:42 GMT
COPY file:ed82059457db34cc43492a36d55b5f9133e36b8d203dcc971bb9feb5fb6a8528 in /nats-server 
# Wed, 04 May 2022 22:01:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:01:43 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:01:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:01:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:01:44 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b04b6f92c475d8e5e8cdec268c94ef3240dde7149afb05913d1099a7ae570a08`  
		Last Modified: Wed, 04 May 2022 22:04:04 GMT  
		Size: 4.2 MB (4237771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef916f73f04fb010ef2bb2bf3b7260ca2d52efb2591d966721af6b5251fd397d`  
		Last Modified: Wed, 04 May 2022 22:04:02 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm variant v7

```console
$ docker pull nats@sha256:5faa61f14caf7dc441f38d86641bd5918d1231b40e7acd0336f57843d8ef704b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4232641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4caf3fcf0c7865ec8500f33783b2ba88253c0e14828b887cc8b103228346c5`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2f9ffa15f39f94a4d8c8c940d7ec0b2baee22852f8f3f2c24a707b69fc8fd84f in /nats-server 
# Wed, 04 May 2022 22:18:15 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 22:18:16 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 22:18:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 22:18:17 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 22:18:17 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:706ff613d28c2f6958458bb4d4ce83f519f2b76bde307418fe1603aac99ac21b`  
		Last Modified: Wed, 04 May 2022 22:20:36 GMT  
		Size: 4.2 MB (4232133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb718277dd458fca567c81e0168c051df2d97f4a8eb0cb348574822d90dec67d`  
		Last Modified: Wed, 04 May 2022 22:20:33 GMT  
		Size: 508.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:scratch` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:009869128938685fc6fee44029ac90758f29d3fc3e33fa7d5e47a7a3905ef115
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4218329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787d12c02030cc31984da44a61d89f3f472271982d215d29866617891286b13`
-	Entrypoint: `["\/nats-server"]`
-	Default Command: `["--config","nats-server.conf"]`

```dockerfile
# Wed, 04 May 2022 21:48:41 GMT
COPY file:8d0405148efb3d718582f81ff5f54494a8c9789f05e85832ee98d04d228af450 in /nats-server 
# Wed, 04 May 2022 21:48:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /nats-server.conf 
# Wed, 04 May 2022 21:48:42 GMT
EXPOSE 4222 6222 8222
# Wed, 04 May 2022 21:48:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/
# Wed, 04 May 2022 21:48:44 GMT
ENTRYPOINT ["/nats-server"]
# Wed, 04 May 2022 21:48:45 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:8d57fa8f4dba3b0b06e2fd0e4e7b35276d5c1078bcf1be00321d6d56bba9aa78`  
		Last Modified: Wed, 04 May 2022 21:50:01 GMT  
		Size: 4.2 MB (4217820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b388c4e085cdf26d57e7c86c2bec5f6519929e7f9ec591330158ba39d77677b4`  
		Last Modified: Wed, 04 May 2022 21:50:00 GMT  
		Size: 509.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore`

```console
$ docker pull nats@sha256:07432a398099039390dadc22e657dfbc8ada5a6475071cdf3a0e7ae97cc5f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:windowsservercore` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:4c410fa02ac3030e41f939d40f93ef6f4b8fa5ef0018742f84ded81ff3dd56f4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509506739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310f6ed1347d5414cbccdf037d24ac72f6a164094e11c88c95c36add4ca70e7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:39:54 GMT
ENV NATS_SERVER=2.8.2
# Wed, 11 May 2022 14:39:55 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.2/nats-server-v2.8.2-windows-amd64.zip
# Wed, 11 May 2022 14:39:56 GMT
ENV NATS_SERVER_SHASUM=300b9743afa50e02e4e8d43dc212bfde8a871617bd524829114e19ff680dde11
# Wed, 11 May 2022 14:40:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 14:41:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 14:41:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:41:58 GMT
EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:41:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705248b3431d43594f02c1a498c5825693a2219dc3e9916401f0c6483917d9a`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb084aa44aefde2d0aa2b439015601202b9289be01b36d72c372e12b207c0e3`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c26ed0b144ad0936998810c48866b8542c5459336cfbc516abbd8e36f335dc`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be12ae5206975ef6a801832e7cb1e13cce3a20a913b8af575d2eb06033f814b`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 482.2 KB (482237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934d847ec8d58fee43acc3f6b9da54c22bbaa3af2fdc22fc6cc7b544df9ed0d`  
		Last Modified: Wed, 11 May 2022 14:42:41 GMT  
		Size: 5.0 MB (4955482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b1d767c6565af1eb4447e5b0ce9d14889a68e438a8f16385c402174fe0d560`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7197706e722c8737fffdee9b04e1f3d7e8e6bc8824673d7f30221ee05c25681`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc51eeff832289639769559e0535687ae4a579b49d847a4fb7236824a8805`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925945a5e74fac0f93b1337cf5af3f61b3b33e549af73c3b2ff6effa8cbe27e4`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `nats:windowsservercore-1809`

```console
$ docker pull nats@sha256:07432a398099039390dadc22e657dfbc8ada5a6475071cdf3a0e7ae97cc5f94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2928; amd64

### `nats:windowsservercore-1809` - windows version 10.0.17763.2928; amd64

```console
$ docker pull nats@sha256:4c410fa02ac3030e41f939d40f93ef6f4b8fa5ef0018742f84ded81ff3dd56f4
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2509506739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1310f6ed1347d5414cbccdf037d24ac72f6a164094e11c88c95c36add4ca70e7`
-	Entrypoint: `["C:\\nats-server.exe"]`
-	Default Command: `["--config","nats-server.conf"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Fri, 22 Apr 2022 01:27:13 GMT
RUN Apply image 10.0.17763.2803
# Thu, 05 May 2022 17:03:24 GMT
RUN Install update 10.0.17763.2928
# Wed, 11 May 2022 12:42:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 11 May 2022 14:39:53 GMT
ENV NATS_DOCKERIZED=1
# Wed, 11 May 2022 14:39:54 GMT
ENV NATS_SERVER=2.8.2
# Wed, 11 May 2022 14:39:55 GMT
ENV NATS_SERVER_DOWNLOAD=https://github.com/nats-io/nats-server/releases/download/v2.8.2/nats-server-v2.8.2-windows-amd64.zip
# Wed, 11 May 2022 14:39:56 GMT
ENV NATS_SERVER_SHASUM=300b9743afa50e02e4e8d43dc212bfde8a871617bd524829114e19ff680dde11
# Wed, 11 May 2022 14:40:42 GMT
RUN Set-PSDebug -Trace 2
# Wed, 11 May 2022 14:41:56 GMT
RUN Write-Host ('downloading from {0} ...' -f $env:NATS_SERVER_DOWNLOAD); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:NATS_SERVER_DOWNLOAD -OutFile nats.zip; 		Write-Host ('verifying sha256 ({0}) ...' -f $env:NATS_SERVER_SHASUM); 	if ((Get-FileHash nats.zip -Algorithm sha256).Hash -ne $env:NATS_SERVER_SHASUM) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 	Write-Host 'extracting nats.zip'; 	Expand-Archive -Path 'nats.zip' -DestinationPath .; 		Write-Host 'copying binary'; 	Copy-Item nats-server-v*/nats-server.exe -Destination C:\\nats-server.exe; 		Write-Host 'cleaning up'; 	Remove-Item -Force nats.zip; 	Remove-Item -Recurse -Force nats-server-v*; 		Write-Host 'complete.';
# Wed, 11 May 2022 14:41:57 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in C:\nats-server.conf 
# Wed, 11 May 2022 14:41:58 GMT
EXPOSE 4222 6222 8222
# Wed, 11 May 2022 14:41:59 GMT
ENTRYPOINT ["C:\\nats-server.exe"]
# Wed, 11 May 2022 14:42:00 GMT
CMD ["--config" "nats-server.conf"]
```

-	Layers:
	-	`sha256:b111c3320c949bea81612bf4554f1b6592c2f504920b5bf57ba340a1d4d52c93`  
		Size: 1.9 GB (1877166088 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:8b534d64a7c337eb8a23b425e4f598cd3e7407ddf8c7b2f714d1e7f7ed6a04be`  
		Size: 626.9 MB (626889777 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b34adcbd607b6c175a7c7a819fecbbfd53899678f53f169f2b4504070ec6b0ab`  
		Last Modified: Wed, 11 May 2022 14:07:06 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee0c1e63aec5d8d83ee6bf4eb10d12ff30fe2e0eee737a2ef9291ead11cfb5cc`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4705248b3431d43594f02c1a498c5825693a2219dc3e9916401f0c6483917d9a`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb084aa44aefde2d0aa2b439015601202b9289be01b36d72c372e12b207c0e3`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c26ed0b144ad0936998810c48866b8542c5459336cfbc516abbd8e36f335dc`  
		Last Modified: Wed, 11 May 2022 14:42:42 GMT  
		Size: 1.4 KB (1419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8be12ae5206975ef6a801832e7cb1e13cce3a20a913b8af575d2eb06033f814b`  
		Last Modified: Wed, 11 May 2022 14:42:43 GMT  
		Size: 482.2 KB (482237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2934d847ec8d58fee43acc3f6b9da54c22bbaa3af2fdc22fc6cc7b544df9ed0d`  
		Last Modified: Wed, 11 May 2022 14:42:41 GMT  
		Size: 5.0 MB (4955482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9b1d767c6565af1eb4447e5b0ce9d14889a68e438a8f16385c402174fe0d560`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 2.0 KB (2001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7197706e722c8737fffdee9b04e1f3d7e8e6bc8824673d7f30221ee05c25681`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c1dc51eeff832289639769559e0535687ae4a579b49d847a4fb7236824a8805`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:925945a5e74fac0f93b1337cf5af3f61b3b33e549af73c3b2ff6effa8cbe27e4`  
		Last Modified: Wed, 11 May 2022 14:42:40 GMT  
		Size: 1.4 KB (1391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
