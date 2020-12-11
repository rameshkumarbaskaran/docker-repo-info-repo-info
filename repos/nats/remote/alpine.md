## `nats:alpine`

```console
$ docker pull nats@sha256:2171f5c92575f14584aaf3c1a6f1d81df197f2a9b884e1f49a9cacdee01b34a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine` - linux; amd64

```console
$ docker pull nats@sha256:bae2212fc958badb823fc4d16be97c8462ef4fac88a21232985d2e0e32b29339
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7176348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03c66868c117154613c3827a8f3d9eab0f23132da65271ad870c69b6295d7fe4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Thu, 22 Oct 2020 02:19:24 GMT
ADD file:f17f65714f703db9012f00e5ec98d0b2541ff6147c2633f7ab9ba659d0c507f4 in / 
# Thu, 22 Oct 2020 02:19:24 GMT
CMD ["/bin/sh"]
# Tue, 03 Nov 2020 00:31:37 GMT
ENV NATS_SERVER=2.1.9
# Tue, 03 Nov 2020 00:31:39 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Tue, 03 Nov 2020 00:31:39 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Tue, 03 Nov 2020 00:31:40 GMT
EXPOSE 4222 6222 8222
# Tue, 03 Nov 2020 00:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 03 Nov 2020 00:31:40 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:188c0c94c7c576fff0792aca7ec73d67a2f7f4cb3a6e53a84559337260b36964`  
		Last Modified: Thu, 22 Oct 2020 02:19:57 GMT  
		Size: 2.8 MB (2796860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80061bc395173316f0e2ac031183f2b19d559a3d6286d2651c67ba46d3262637`  
		Last Modified: Tue, 03 Nov 2020 00:32:22 GMT  
		Size: 4.4 MB (4378545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c137c6b14b00714d6980c52fd66b87dad6326532ee73d9d30afcef1df7c3c2e`  
		Last Modified: Tue, 03 Nov 2020 00:32:20 GMT  
		Size: 529.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7953a59047cda9561df26c70a01028ff29320e205d6c3115efe94879f98b98b7`  
		Last Modified: Tue, 03 Nov 2020 00:32:21 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v6

```console
$ docker pull nats@sha256:6503ed588fc096e977bb922b348a07f4d4905370c1e5889e461d72c60c923041
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.7 MB (6702193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf2171ba185c9f29a81c567a67012c850b75459c092964c08768b2eb47187fae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 11 Dec 2020 02:17:15 GMT
ADD file:1a9c0a67560d338c0c0e7005d8915d998fc9cf3e9f53bfd7e42e8391f0a39bce in / 
# Fri, 11 Dec 2020 02:17:15 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 04:44:37 GMT
ENV NATS_SERVER=2.1.9
# Fri, 11 Dec 2020 04:44:41 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 11 Dec 2020 04:44:42 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 11 Dec 2020 04:44:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 11 Dec 2020 04:44:43 GMT
EXPOSE 4222 6222 8222
# Fri, 11 Dec 2020 04:44:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 04:44:44 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f1c16df8fee33d421d08790b17ca2af67a3fe49e77b6b991dd0c30631f5d1baf`  
		Last Modified: Fri, 11 Dec 2020 02:17:57 GMT  
		Size: 2.6 MB (2601992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21a695900646e7f37d5ce8031ca05cf06af5d6579d98437d49f3a4b3b740e330`  
		Last Modified: Fri, 11 Dec 2020 04:45:21 GMT  
		Size: 4.1 MB (4099231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fcd5c1d3aba3080ccf692bc54feb76f1328e2f9cbb91198e7850f2bb877e65`  
		Last Modified: Fri, 11 Dec 2020 04:45:21 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a06d4563b2d381a932abe23c6a907b4bbc7506ad6c26befe8015da3fc6a8a06`  
		Last Modified: Fri, 11 Dec 2020 04:45:20 GMT  
		Size: 412.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm variant v7

```console
$ docker pull nats@sha256:a5dc968d176a219c54a707db048ed0fbd70a996425410780e6a52e35ba3d2b87
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.5 MB (6501306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:72e90e5a73fb939a32f56c03dfe1fa3aa7e739f4c1e232f0977c34f4030725d3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 11 Dec 2020 02:20:33 GMT
ADD file:0e85952ec585d17378d9bb15a94ddc10c3ed8f766f275cf50fb36be1126f35d2 in / 
# Fri, 11 Dec 2020 02:20:34 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:07:47 GMT
ENV NATS_SERVER=2.1.9
# Fri, 11 Dec 2020 05:07:56 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 11 Dec 2020 05:07:58 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 11 Dec 2020 05:07:59 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 11 Dec 2020 05:08:00 GMT
EXPOSE 4222 6222 8222
# Fri, 11 Dec 2020 05:08:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:08:03 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:f70c74f2e22556cebd0cbbff78c03d4f0560d76979bf799d67730340a639aa57`  
		Last Modified: Fri, 11 Dec 2020 02:21:18 GMT  
		Size: 2.4 MB (2405692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebd2f164f3205daa3d917523e7edd465184d54721686a4bdfd8735877659b849`  
		Last Modified: Fri, 11 Dec 2020 05:08:42 GMT  
		Size: 4.1 MB (4094643 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:805d7ecd6f5d7e65e965ee249efd25a355081a6ecaafee6ea4073dda945c385f`  
		Last Modified: Fri, 11 Dec 2020 05:08:41 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ee50d53a833948de3fddbcd198ca411803f47b5e5c1ef34173a72ddcd118e76`  
		Last Modified: Fri, 11 Dec 2020 05:08:40 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:7fe5038348b0276f0e719c39bad479a55a0f8e18c345a6969fc3791a7e8a76ea
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6786403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca6f724dcaa3fa340a2b07a21c641d9f2543d6070585778f748e08fb9fbbe792`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Fri, 11 Dec 2020 02:42:58 GMT
ADD file:a1a6d0f8dffb9bc75438921cdb5c04d2f2f49400a7526dcf3d8dff9238e3235a in / 
# Fri, 11 Dec 2020 02:43:00 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 05:18:36 GMT
ENV NATS_SERVER=2.1.9
# Fri, 11 Dec 2020 05:18:42 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='22659ec3653a2db53294427c8ec939a3b9d207a36ea54daf945b9fa43477434d' ;; 		armhf) natsArch='arm6'; sha256='761d1062303e9637196ab3b329d01609ea907d297e6c10f6932212b62ff9b1b4' ;; 		armv7) natsArch='arm7'; sha256='0a000c41c5031969f7b855cf4c65d5e6b1d6cd2230857f728a190a6ee128828c' ;; 		x86_64) natsArch='amd64'; sha256='c9538f4a47ffe75d11f3c5ce1e1c9a3c6ae1e26e26f7a1428ca5dda6b1b476d1' ;; 		x86) natsArch='386'; sha256='079cbfc5f42ebbe2b696fdc88c75ffdebd3b9f34e88d61a829ced064ab48a749' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Fri, 11 Dec 2020 05:18:43 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Fri, 11 Dec 2020 05:18:43 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Fri, 11 Dec 2020 05:18:44 GMT
EXPOSE 4222 6222 8222
# Fri, 11 Dec 2020 05:18:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 11 Dec 2020 05:18:46 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:a3cc7d3b244e0bac4f32b7529f804d1ab735b088ea432061c3949b2a890b919f`  
		Last Modified: Fri, 11 Dec 2020 02:43:46 GMT  
		Size: 2.7 MB (2706619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd3d49df80e6f74b5a23e2b839fc303f88b22a34222381e79cd98149c1754c74`  
		Last Modified: Fri, 11 Dec 2020 05:19:28 GMT  
		Size: 4.1 MB (4078814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0254ed8b78cd9b9b81a26b7e6762d50edd6f0410667b89320924a3f60bd48df8`  
		Last Modified: Fri, 11 Dec 2020 05:19:25 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2ccea82e44f4bdd0a187f4cbf2bf4e0d1a896d1215875febf4ac2fc866819d`  
		Last Modified: Fri, 11 Dec 2020 05:19:26 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
