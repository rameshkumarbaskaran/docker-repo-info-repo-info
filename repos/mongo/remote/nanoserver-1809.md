## `mongo:nanoserver-1809`

```console
$ docker pull mongo@sha256:92307e630649513c53d0faab70318170386eceab554996201c707a78fa25c33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `mongo:nanoserver-1809` - windows version 10.0.17763.4737; amd64

```console
$ docker pull mongo@sha256:45cbd94e9a43424c6bb0cecaba6aa6398fa75c8c57e7031090c2675c9a5efdd4
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **716.5 MB (716474626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b822b1f867746dbd0faf3e76a56a67fa43bf939b9ea5c3789904fcd826b54df4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Thu, 10 Aug 2023 00:48:08 GMT
SHELL [cmd /S /C]
# Thu, 10 Aug 2023 01:15:48 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 01:15:57 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Thu, 10 Aug 2023 01:15:57 GMT
USER ContainerUser
# Thu, 10 Aug 2023 01:15:58 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 06 Sep 2023 00:42:19 GMT
ENV MONGO_VERSION=7.0.1
# Wed, 06 Sep 2023 00:43:08 GMT
COPY dir:dd7e8197ac0171161d6946ee93a67cf7f770b5ce539a9dc154869493c9e2623b in C:\mongodb 
# Wed, 06 Sep 2023 00:43:26 GMT
RUN mongod --version
# Wed, 06 Sep 2023 00:43:26 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 06 Sep 2023 00:43:27 GMT
EXPOSE 27017
# Wed, 06 Sep 2023 00:43:28 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:298e0f667b1d8252956bc07b8438d68801dd9eb4ebb7ad345fde0bed30609680`  
		Last Modified: Thu, 10 Aug 2023 01:03:59 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:814fa0d01fded994ad965ae5487dc312820ecd968291d0bb20ee608f702a9689`  
		Last Modified: Thu, 10 Aug 2023 02:00:40 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b021e83a508dc7adbef323d416f3a04d3d4889d441750fa4ecf3ed425ee2e1f0`  
		Last Modified: Thu, 10 Aug 2023 02:00:39 GMT  
		Size: 69.2 KB (69188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956b7c3ad022ed0da478f25e9b64d0c5ac7947ac14c611b3d359ef414b7abf35`  
		Last Modified: Thu, 10 Aug 2023 02:00:38 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faf6796c7b91221863b1920e4991f4a08153b38f271641d2b9cd3ab35640e935`  
		Last Modified: Thu, 10 Aug 2023 02:00:38 GMT  
		Size: 267.2 KB (267155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af7865829a801a91fb2c09e52097838c59ada366288cbd1916bfb7382d9593e4`  
		Last Modified: Wed, 06 Sep 2023 00:59:45 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8de58d02de8efb28abf904fed2cf1caeb94f6908441c79fd6c88644d6e2f0fc`  
		Last Modified: Wed, 06 Sep 2023 01:01:12 GMT  
		Size: 611.6 MB (611589254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47438ddb25bf4b8bc185fee073f6f48934b605783d7c35fce0c458be57cd4631`  
		Last Modified: Wed, 06 Sep 2023 00:59:43 GMT  
		Size: 81.6 KB (81555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698297bd93c96c5384e274769db441e7593c5b0a8debcc5b1b0bb8e5b310b7fb`  
		Last Modified: Wed, 06 Sep 2023 00:59:43 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6363f3147ce7d67ddac7741ba520355a07930b6c35c52447ba23f9169973a873`  
		Last Modified: Wed, 06 Sep 2023 00:59:43 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0b94ce87ed29d69b719c3e8b4bd12831f502c832b08d5f026e0b4e8838a959`  
		Last Modified: Wed, 06 Sep 2023 00:59:43 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
