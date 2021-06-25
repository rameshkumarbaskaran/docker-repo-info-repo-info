## `nats:alpine3.13`

```console
$ docker pull nats@sha256:9b9adec140c2d092472a75f068117db59743075cd056ab55469206d9562513b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8

### `nats:alpine3.13` - linux; amd64

```console
$ docker pull nats@sha256:11ac3d707fd53db8987f4e5432397c58bcd7fcd98e9c056088f709a58b4fc3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7428242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2523bcf697d78fbb44315448e0c04248daa07f5741fc4c1d82224203a3a1a982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 18:20:14 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 18:20:17 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 18:20:17 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 18:20:17 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 18:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 18:20:18 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db7669d67fb4cfb54da583e883237da0b279b1fb366b087a0a503ca26d962042`  
		Last Modified: Thu, 24 Jun 2021 18:21:21 GMT  
		Size: 4.6 MB (4615300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14a63d38912003c0b7e278dc2e07a5e3595d926f114688e1eba7453d10771507`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50aa5d23eab2b64578272b85b1840118f8ce74d4c8a076fd9fdbbf112b389a15`  
		Last Modified: Thu, 24 Jun 2021 18:21:20 GMT  
		Size: 415.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v6

```console
$ docker pull nats@sha256:afafd733f206092cfbf83b03d0d219e3ad9fc986d7b9bd1bcc813ba9a164e831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6897059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39a08095811cc4b9caf05423603dec24983d69af81a39a2b582c3fed0698cbcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:17:03 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:17:08 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:17:08 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:17:09 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:17:09 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:17:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:17:10 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072466ad1c8b3759328223593e85cddeedd93281cc285d4fbcc43c2aa77cff8b`  
		Last Modified: Thu, 24 Jun 2021 19:19:11 GMT  
		Size: 4.3 MB (4273957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040948b8c4aa41212a8812f47174f14427d9e2e336d534553442231f4f521882`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 557.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7ac2240a33c4d9b574bff55265289f9093dcbe62577c93ce04d3b9b145e45e`  
		Last Modified: Thu, 24 Jun 2021 19:19:08 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm variant v7

```console
$ docker pull nats@sha256:6f98f2a6b2a351cda8094822e8cca03c241a3f0ba26fb0baa36a7d4a7859e161
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6617713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:633f445cf47953e0ee9347ad2b0f944a3877dc8de52142ca91a56265e587b9c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 23:15:15 GMT
ADD file:028c5b473d862250586e174c5dd19b37f8fc3bffbc02d888e72df30f32fd6129 in / 
# Tue, 15 Jun 2021 23:15:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Jun 2021 13:20:33 GMT
ENV NATS_SERVER=2.2.6
# Wed, 16 Jun 2021 13:20:36 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='779d7f363fb0244071e67bf146c7169a8e3c35af2746c0a01323a3c5fd12bf31' ;; 		armhf) natsArch='arm6'; sha256='ed7211f56fa3928e3664ed92df632b0e7480bd1b4a91c239cb26a0f55831c815' ;; 		armv7) natsArch='arm7'; sha256='a55335b1329248912e80d8e68b5dd6b6a48c4742de089c4226f503d7e8357f2c' ;; 		x86_64) natsArch='amd64'; sha256='fc67ce0b4c748fa16ff92414c7d6be18a9285824c21d9629684c0093cf074f77' ;; 		x86) natsArch='386'; sha256='386811034531cea6e794e4764fdd70b0b948fdf7212064e8c176663992c46f2e' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.zip "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.zip"; 	echo "${sha256} *nats-server.zip" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp unzip; 		unzip nats-server.zip "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server"; 	rm nats-server.zip; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rmdir "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Wed, 16 Jun 2021 13:20:36 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Wed, 16 Jun 2021 13:20:37 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Wed, 16 Jun 2021 13:20:37 GMT
EXPOSE 4222 6222 8222
# Wed, 16 Jun 2021 13:20:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 16 Jun 2021 13:20:37 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:e160e00eb35d5bc2373770873fbc9c8f5706045b0b06bfd1c364fcf69f02e9fe`  
		Last Modified: Wed, 14 Apr 2021 18:58:36 GMT  
		Size: 2.4 MB (2424145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53cb7c99153233d7f9f99a7aca1307855f9a7dac7819cbddadda08fbd99ec601`  
		Last Modified: Wed, 16 Jun 2021 13:22:14 GMT  
		Size: 4.2 MB (4192596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5d234a6a1f8b69e2c7ee006b8d462ddb4a7bf8b8d2bf85cbe2eef01a55d4a49`  
		Last Modified: Wed, 16 Jun 2021 13:22:13 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2064be6393f59c7917d1eb568267a13b636f128298f96dd8f1990c6cf105fac9`  
		Last Modified: Wed, 16 Jun 2021 13:22:14 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nats:alpine3.13` - linux; arm64 variant v8

```console
$ docker pull nats@sha256:e7be6da297d4e47e1cbf0cebebb0b28db6ceeb50f8e06e87609dce41de682f92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6953599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0539985a8e92b6e078f0f65ffce3ff416cfa3401034c750ec07b9da7150efce8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["nats-server","--config","\/etc\/nats\/nats-server.conf"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 24 Jun 2021 19:06:45 GMT
ENV NATS_SERVER=2.3.0
# Thu, 24 Jun 2021 19:06:48 GMT
RUN set -eux; 	apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		aarch64) natsArch='arm64'; sha256='139521edba99389436c95b12b93aa4e7fbc0b2d07ac8584902cfc4d417773d3c' ;; 		armhf) natsArch='arm6'; sha256='ebc1907729fa322c1191ce605e55c54f063bacf5f811802e8a32076210131975' ;; 		armv7) natsArch='arm7'; sha256='30476c49ca5f1404b7bc3536ad325da9d8c7eb6f733c1b992fc20bf288e15eeb' ;; 		x86_64) natsArch='amd64'; sha256='3a6097371169d750d73b643f2d4644b99e575e966a99e8458426bbfccb8fda7b' ;; 		x86) natsArch='386'; sha256='37715ed91c4a3698fde4ba69f2bf8fd3cd1346347bbab97f3af176cdbcb47b05' ;; 		*) echo >&2 "error: $apkArch is not supported!"; exit 1 ;; 	esac; 		wget -O nats-server.tar.gz "https://github.com/nats-io/nats-server/releases/download/v${NATS_SERVER}/nats-server-v${NATS_SERVER}-linux-${natsArch}.tar.gz"; 	echo "${sha256} *nats-server.tar.gz" | sha256sum -c -; 		apk add --no-cache ca-certificates; 	apk add --no-cache --virtual buildtmp; 		tar -xf nats-server.tar.gz; 	rm nats-server.tar.gz; 	mv "nats-server-v${NATS_SERVER}-linux-${natsArch}/nats-server" /usr/local/bin; 	rm -rf "nats-server-v${NATS_SERVER}-linux-${natsArch}"; 		apk del --no-cache --no-network buildtmp
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:bef66f144841968228eb6875fdca1fb9c094da90455a3e05090bdd09e690e7ea in /etc/nats/nats-server.conf 
# Thu, 24 Jun 2021 19:06:48 GMT
COPY file:b2810cc282a84164c4e1e5f77556bd78260283c00b329045f3f64a63f71e3570 in /usr/local/bin 
# Thu, 24 Jun 2021 19:06:48 GMT
EXPOSE 4222 6222 8222
# Thu, 24 Jun 2021 19:06:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 24 Jun 2021 19:06:49 GMT
CMD ["nats-server" "--config" "/etc/nats/nats-server.conf"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27d0993acd4f2a9aa99219b53b130917cfcaa7b5ab8f75f92c6853892b1fbd8`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 4.2 MB (4240601 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b89210891c944f9ecbd826fe696a7f0a1399ac8628705331d9eb011d633fe7b2`  
		Last Modified: Thu, 24 Jun 2021 19:08:01 GMT  
		Size: 558.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e288f0bb2545133bb23a02793719cdc1076dc77f7c61c80c05c6351f9dc2c482`  
		Last Modified: Thu, 24 Jun 2021 19:08:02 GMT  
		Size: 414.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
