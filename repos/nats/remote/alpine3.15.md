## `nats:alpine3.15`

```console
$ docker pull nats@sha256:6f256e859cd7360110891e76790893995991815ee144a0fcf21561c359c2fa1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.15` - linux; amd64

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

### `nats:alpine3.15` - linux; arm variant v6

```console
$ docker pull nats@sha256:8b48b81efe06e10f92980ce446aa199c35e591e6e61f6a508e8e5b83b993c75c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.1 MB (7141581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3fcaa7e9654b63fb8642995444c1d4e0c884d6bfc2a16fdb8a7a39e137b5208`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:42 GMT
ADD file:159dcddaab900372df882a4e94615ed84250e9cea3e74bc0479d98280342f596 in / 
# Mon, 04 Apr 2022 23:49:42 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:55:37 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:55:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:55:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:55:42 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:55:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:55:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:55:43 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c319b1fc4ed70b8241a7ce6ac0c4015d354bf5cf8c01eb73c50b6709c0c46e49`  
		Last Modified: Mon, 04 Apr 2022 19:09:22 GMT  
		Size: 2.6 MB (2621972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d50f68c47a108ab599d7f0e191ffaf378e6dce6a928151e691d8ea726aeb928`  
		Last Modified: Thu, 26 May 2022 23:57:46 GMT  
		Size: 4.5 MB (4518611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4cb9d5e8d247c55e5f7e46c8d54ea485f55806c24444feaf62725d6ba170f1`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 585.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:137c6a3cdd4a881f42229288ebba9a675d7abe171cd2b2838becae58d1aad6ab`  
		Last Modified: Thu, 26 May 2022 23:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm variant v7

```console
$ docker pull nats@sha256:aa130a56f0b1428fc47e92102e4273d7cbff4b90534b8b134b2d658a6d1c38bf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6938699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d68a57086629ed4e52dfa052c8b25706377fa32c9fb518fe4f8d3b74ba922f50`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:57:34 GMT
ADD file:20f8cdddc53a4a8bd78945fc32fe08e9f80ab3b16dc20a9aa4ba73b79f2bc71c in / 
# Mon, 04 Apr 2022 23:57:35 GMT
CMD ["/bin/sh"]
# Mon, 23 May 2022 23:30:41 GMT
ENV NATS_SERVER=2.8.3
# Mon, 23 May 2022 23:30:45 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='905df5647dba0443ce6b92116ff5c6ceb49d3e24fa78c999d0c19fe634f341d6' ;; 		armhf) natsArch='arm6'; sha256='590a0460362ab1fc47ebce8886f5a53ff8b91abefa412ce77762f8514041394b' ;; 		armv7) natsArch='arm7'; sha256='142673f4eafca832e0347b1be0f5f9b0b7b23a46c08a623b63c6925a94a2d9f1' ;; 		x86_64) natsArch='amd64'; sha256='16e6bfa14e8ba9bc7d924e296bfe6bcad803b04318e6d60ef14ee45e3d3ddc60' ;; 		x86) natsArch='386'; sha256='fc749ab7574aa9ae22661a89ad73ac26331772e2302197d1625db56e967a74ac' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Mon, 23 May 2022 23:30:45 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Mon, 23 May 2022 23:30:46 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Mon, 23 May 2022 23:30:46 GMT
EXPOSE 4222 6222 8222
# Mon, 23 May 2022 23:30:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 23 May 2022 23:30:47 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:57fb4b5f1a47c953ca5703f0f81ce14e5d01cf23aa79558b5adb961cc526e320`  
		Last Modified: Mon, 04 Apr 2022 19:09:36 GMT  
		Size: 2.4 MB (2424323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a80fca66b8067494cea5416b87c794783f42324795d17be4972cfaed3c14c44`  
		Last Modified: Mon, 23 May 2022 23:32:55 GMT  
		Size: 4.5 MB (4513374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf8c7c58b8c4cd539401a48d23026f9d28d2e99bad1997337a5cc45321f8873`  
		Last Modified: Mon, 23 May 2022 23:32:52 GMT  
		Size: 586.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99a96a070c80e547148535de9946c1f98e6d8d8dfa7fe6ae1c51e269930f1e61`  
		Last Modified: Mon, 23 May 2022 23:32:52 GMT  
		Size: 416.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.15` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:068170580c70c9c06e2050fa9c6f66ec28f61c9062663cf2b45db2eed7e6b3d6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7218027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45fa83e475ee42455e6e7021633d7a98bb6496a5a75621f389dff13b1ceaa343`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:31 GMT
ADD file:90e56af13188c7f0283d244a0d70b853d8bef8587a41f1da8eac3a2aba8964ef in / 
# Mon, 04 Apr 2022 23:39:31 GMT
CMD ["/bin/sh"]
# Thu, 26 May 2022 23:53:38 GMT
ENV NATS_SERVER=2.8.4
# Thu, 26 May 2022 23:53:40 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='75a53e10c640c8348bafe43300785d5147c91f60cd721c21ec896bc50727270a' ;; 		armhf) natsArch='arm6'; sha256='993a0d02ff9d0c74be31dc9e7ac1066659637c4897cc94ced2e0dc982fb428f3' ;; 		armv7) natsArch='arm7'; sha256='89e4191a0bc15c2196f2e6c1b2a3c4200576f6e8ec1176060b2a191c5e588b0d' ;; 		x86_64) natsArch='amd64'; sha256='da8c999ab0da5881fde68cba55238748d7310f28022fb78b9c07b420572a4b45' ;; 		x86) natsArch='386'; sha256='e94e5ec1076122e782527f4a98937c60c9eed4d04c6ba0364986cc58cd3ff8f8' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 26 May 2022 23:53:42 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 26 May 2022 23:53:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 26 May 2022 23:53:43 GMT
EXPOSE 4222 6222 8222
# Thu, 26 May 2022 23:53:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 26 May 2022 23:53:45 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:9981e73032c8833e387a8f96986e560edbed12c38119e0edb0439c9c2234eac9`  
		Last Modified: Mon, 04 Apr 2022 19:09:10 GMT  
		Size: 2.7 MB (2716477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e48649cc80ad9a6544bde7c572f66e6a5f2c0e918923a957045cfea77bbf31bb`  
		Last Modified: Thu, 26 May 2022 23:54:50 GMT  
		Size: 4.5 MB (4500578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43bbb498a8d1c04c80271b66119f843bc9a68cf260f1fc0005babdb8ef1820b8`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 559.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:922ca2313cb9b3e722a83aa9f01456f583d124cbb90aa75908b33a0c37ecdaeb`  
		Last Modified: Thu, 26 May 2022 23:54:49 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
