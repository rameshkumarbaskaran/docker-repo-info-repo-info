## `nats:2-alpine3.17`

```console
$ docker pull nats@sha256:c0ffa1bed32d05eebcbc9892ecfa0c37ea9f1139ef480d1bc6c8c031a8d2a78e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:2-alpine3.17` - linux; amd64

```console
$ docker pull nats@sha256:4455732015639b8c2fa8e9020f3d17e8a209f9d59543292710768af952148382
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8581793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3b6d7d2a01e46a077c00066353ec8f59dd1f7812c8dd98a987f5250bbd6b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:19:28 GMT
ADD file:587cae71969871d3c6456d844a8795df9b64b12c710c275295a1182b46f630e7 in / 
# Tue, 22 Nov 2022 22:19:29 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:34:51 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:34:54 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:34:54 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:34:54 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:34:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:34:55 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c158987b05517b6f2c5913f3acef1f2182a32345a304fe357e3ace5fadcad715`  
		Last Modified: Tue, 22 Nov 2022 22:19:52 GMT  
		Size: 3.4 MB (3370706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed86478665b1337795c7e912325131cdc2d168214502eed69e3723ff4a234d25`  
		Last Modified: Thu, 08 Dec 2022 20:36:07 GMT  
		Size: 5.2 MB (5210085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c69220328c19fd2b50424c54dca1d8a7b058aa5a162eb5ac14521e35c4d62f1a`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b79d3be31b99b819fb19f51849bff6e77c2b09db3e5da0d0ef4e094ed967ff8f`  
		Last Modified: Thu, 08 Dec 2022 20:36:06 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm variant v6

```console
$ docker pull nats@sha256:3119056346819803bc76df59c2e831ff5171a8da1f002a4607e7e2abfbe6ecee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8082503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc75fd6f64f71d7f3e687447b6480cd6f9d57bd8a4ba7c2983d8861d4e3b51d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:55:46 GMT
ADD file:132c76d7f7dae2f51f589ee460f1870a2cec6e9dc7ff8e38e88fcee2cfbe70da in / 
# Tue, 22 Nov 2022 22:55:46 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:59:56 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:59:59 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:59:59 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:00:00 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:00:00 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:00:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:00:00 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:c2eb4db52fbe1266a78d8c185d33544a2916faa7d82fb5f50909fe233e0579da`  
		Last Modified: Tue, 22 Nov 2022 22:56:39 GMT  
		Size: 3.1 MB (3107138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f27e96bda80af22fdcbc14d587a8bd7f1785a53f6186c176c60cb5ee041552`  
		Last Modified: Thu, 08 Dec 2022 20:01:16 GMT  
		Size: 5.0 MB (4974390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d3bcb78d13a5f28e8655978e2d55ca50e33f3c13cd5c589ed9ff1af70a7316f`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 560.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:495e1ec935b2a91f7057d7585b3674b8243a942618d53d46882d39f719432979`  
		Last Modified: Thu, 08 Dec 2022 20:01:15 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm variant v7

```console
$ docker pull nats@sha256:5831f8c5ef78543c5468a18f140d4437b908d992d4d902ede67b681ae1b9d368
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7831737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a580d362e6b152069cf3b30f5e629c7e3b964a990c4a7d15e5e5c33bf6f9610a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:57:20 GMT
ADD file:080010d9005e8e0dae3e98c7f9afff3e3a40ed32579ca01946efc6ede8316bad in / 
# Tue, 22 Nov 2022 22:57:20 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 20:30:58 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 20:31:02 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 20:31:02 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 20:31:02 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 20:31:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 20:31:02 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:cb2ec849933dd31db64abae3fdcb6923c490d9795577bee1ee1be04eab0376ee`  
		Last Modified: Tue, 22 Nov 2022 22:58:12 GMT  
		Size: 2.9 MB (2865346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:671c89e40ba9d510918522256afe00ea4e39a695355982e9f361339ed50f7d08`  
		Last Modified: Thu, 08 Dec 2022 20:32:23 GMT  
		Size: 5.0 MB (4965424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0de0969a38fcc2a8858b856efe0a63cd2745e3618c370383bea1f20db57e5e0c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 556.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d0563d82f6dafe5dc45f3a674812a38a28ae6df2f7ac30a4d7664811a572c`  
		Last Modified: Thu, 08 Dec 2022 20:32:22 GMT  
		Size: 411.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:2-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:d6a6c27b86493e468a184154633dfddf07e4fe466ad39c6b7eeaa4609e2ed0d2
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8056469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3378f00ddf68731dab0ff2d503395918d1b20713f78c76e5e28bdf22fc29d78f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 22 Nov 2022 22:39:21 GMT
ADD file:685b5edadf1d5bf0aeb2aec35f810d83876e6d2ea0903b213f75a9c5f0dc5901 in / 
# Tue, 22 Nov 2022 22:39:21 GMT
CMD ["/bin/sh"]
# Thu, 08 Dec 2022 19:56:52 GMT
ENV NATS_SERVER=2.9.9
# Thu, 08 Dec 2022 19:56:55 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='6c0bfc475521c54df3602171a8229d07ff24520f2e7ea7788788e20d01b3b657' ;; 		armhf) natsArch='arm6'; sha256='cc41956b152d942c892cfbcee1f0ab9c632b4729b9bb53962c89e11701ac4458' ;; 		armv7) natsArch='arm7'; sha256='c246ea76e20d0265de10c8af81b4b19c9659401b5ec68db0b04422bd92d273ab' ;; 		x86_64) natsArch='amd64'; sha256='e1e0e4bf2bc731aa63508c6794cc454a085aedb120752e51ecfe3951bfae9fde' ;; 		x86) natsArch='386'; sha256='961c820aad39a095e324704e9305b9311c66599f3cabee0e6d4aba701fae8521' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}";
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:2c51166f33066351f3cfe3734f884c41f36fb66575bdde453c5c93e819cfae35 in /etc/nats/nats-server.conf 
# Thu, 08 Dec 2022 19:56:55 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 08 Dec 2022 19:56:55 GMT
EXPOSE 4222 6222 8222
# Thu, 08 Dec 2022 19:56:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 08 Dec 2022 19:56:56 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:261da4162673b93e5c0e7700a3718d40bcc086dbf24b1ec9b54bca0b82300626`  
		Last Modified: Tue, 22 Nov 2022 22:39:45 GMT  
		Size: 3.3 MB (3259190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:986444278dadde0d9a262ed4b893f80ad454eb35ffc857e42b5ad2f073465016`  
		Last Modified: Thu, 08 Dec 2022 19:57:44 GMT  
		Size: 4.8 MB (4796278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f5d8e79ec79a470e91e51e5aa1553566f49b677c12044d8e9b5c796e0ee27e`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 588.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4e306fd7736484456b60e0960d6d29025a49f82670bf70fad13a464afa6aec`  
		Last Modified: Thu, 08 Dec 2022 19:57:43 GMT  
		Size: 413.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
