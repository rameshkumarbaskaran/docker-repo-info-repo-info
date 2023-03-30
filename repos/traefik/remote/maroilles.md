## `traefik:maroilles`

```console
$ docker pull traefik@sha256:5d47b7bb25467dbc27ab2b260e496a7f9e1232511af369cdcc98daefba7979c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8

### `traefik:maroilles` - linux; amd64

```console
$ docker pull traefik@sha256:d7bacaf9ca8d59b0e7c304920629d98bb98a545127ca4b10e16c8b252b9351b9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22593766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aae4b2c164f286aeee70180f0b85a66a5a3652a07d87cc658851db5e53c9b59a`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Fri, 07 Oct 2022 04:21:33 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 30 Mar 2023 02:37:59 GMT
COPY dir:fcb1de0a76c41fc3dff8d6ca27f999d211e86842b0843ac2ebdecb15ff8e0492 in /usr/share/ 
# Thu, 30 Mar 2023 02:38:00 GMT
COPY file:36217e5a6056bef26cfff395c8af8c1010a61dbe8d62b2c7869ca221e2a6302c in / 
# Thu, 30 Mar 2023 02:38:01 GMT
EXPOSE 80
# Thu, 30 Mar 2023 02:38:01 GMT
VOLUME [/tmp]
# Thu, 30 Mar 2023 02:38:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 30 Mar 2023 02:38:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:39006e619508cd8a1ace2dcb57ecaa3a206fc01c9b72018e30b538ba58b0f45a`  
		Last Modified: Fri, 07 Oct 2022 04:22:39 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ed5475338aea0040268938cdb4cf5e6d08120622d034f2fe282ade7fb88f34`  
		Last Modified: Thu, 30 Mar 2023 02:39:32 GMT  
		Size: 308.3 KB (308275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62941aba458e9caf3e4a66617f7b97e463e427c1ee961fbc3b0a37b3dedaf385`  
		Last Modified: Thu, 30 Mar 2023 02:39:36 GMT  
		Size: 22.2 MB (22161951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm variant v6

```console
$ docker pull traefik@sha256:0eba228e1865efa7bed0cd8ca41b7d6cf14dcab9f1852e3754b7815aeded5d20
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21055086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cd7b650b4ab04f4e437d8c394fb6f2190aea6b3e738817ce9f2462a9d93211`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Tue, 14 Mar 2023 01:31:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 30 Mar 2023 00:40:30 GMT
COPY dir:fcb1de0a76c41fc3dff8d6ca27f999d211e86842b0843ac2ebdecb15ff8e0492 in /usr/share/ 
# Thu, 30 Mar 2023 00:40:31 GMT
COPY file:5d1e7e81e8b77b4f8828eeaf0d30a0f135a949b51396f12ae22af376c36d3129 in / 
# Thu, 30 Mar 2023 00:40:32 GMT
EXPOSE 80
# Thu, 30 Mar 2023 00:40:32 GMT
VOLUME [/tmp]
# Thu, 30 Mar 2023 00:40:32 GMT
ENTRYPOINT ["/traefik"]
# Thu, 30 Mar 2023 00:40:32 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:68a2bb2e7a38ecc0a394b8fde6e116d903af0a9081c1816df304ab9a95b081da`  
		Last Modified: Tue, 14 Mar 2023 01:34:18 GMT  
		Size: 123.5 KB (123540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae617ce90fe46cea74fe5b74b5c0b409ee3f81c32e2bb9f1aefe371e24ebccc1`  
		Last Modified: Thu, 30 Mar 2023 00:42:02 GMT  
		Size: 308.3 KB (308265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296e5dd1d0ad1bc244926e357696aac4774dcebeb52a2723b33bf9269b3df2db`  
		Last Modified: Thu, 30 Mar 2023 00:42:06 GMT  
		Size: 20.6 MB (20623281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `traefik:maroilles` - linux; arm64 variant v8

```console
$ docker pull traefik@sha256:324f12be044568e2f6d8229c848734927a52950051372f956304692aa2ff1a58
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20563152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b41da85c4671491cd2a55c06fe1efb206c993b03f2d5f02f5113268616bf0f04`
-	Entrypoint: `["\/traefik"]`

```dockerfile
# Thu, 27 Oct 2022 23:00:59 GMT
COPY file:48964762d0c961c28f59ebd3ea194fb6486cf2bd9a9cf1780f6702d88bd7b7d9 in /etc/ssl/certs/ 
# Thu, 30 Mar 2023 03:27:00 GMT
COPY dir:fcb1de0a76c41fc3dff8d6ca27f999d211e86842b0843ac2ebdecb15ff8e0492 in /usr/share/ 
# Thu, 30 Mar 2023 03:27:01 GMT
COPY file:60330593b6644f3f519fd13ce8ee34c2c7ab9994a1420afabbc01926dd1230dd in / 
# Thu, 30 Mar 2023 03:27:01 GMT
EXPOSE 80
# Thu, 30 Mar 2023 03:27:01 GMT
VOLUME [/tmp]
# Thu, 30 Mar 2023 03:27:01 GMT
ENTRYPOINT ["/traefik"]
# Thu, 30 Mar 2023 03:27:01 GMT
LABEL org.opencontainers.image.vendor=Traefik Labs org.opencontainers.image.url=https://traefik.io org.opencontainers.image.title=Traefik org.opencontainers.image.description=A modern reverse-proxy org.opencontainers.image.version=v1.7.34 org.opencontainers.image.documentation=https://docs.traefik.io
```

-	Layers:
	-	`sha256:384a668e636c3a58c260d7eacd140f07b0727673d5ba128334cbcedd184a99f2`  
		Last Modified: Thu, 27 Oct 2022 23:02:00 GMT  
		Size: 123.5 KB (123538 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcae1c052addf1a94540e967bada340c12bef5e3c6fa1fd315bdc81f3e2db29b`  
		Last Modified: Thu, 30 Mar 2023 03:28:23 GMT  
		Size: 308.3 KB (308267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a42d66bc2a6eaad18db8aeaaba24844b6f3fcb88954cbef25552a284d0c967de`  
		Last Modified: Thu, 30 Mar 2023 03:28:26 GMT  
		Size: 20.1 MB (20131347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
