## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:4189a2b614a1bcd22ec39bd54df918d315d179a4abaa7eba1ea97fe653f8def9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1787; amd64
	-	windows version 10.0.17763.4499; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.1787; amd64

```console
$ docker pull mongo@sha256:2f6da9886e38c60eb08d7e373f2af68ea13edc655ba63b4107dea092d269e494
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.5 MB (365480720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745d3040be815427c99d6a5916df3c0f1ae402dcd0a1e73493afabc164b8a21b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 21 Jun 2023 07:39:21 GMT
RUN Apply image 10.0.20348.1787
# Sat, 24 Jun 2023 01:47:25 GMT
SHELL [cmd /S /C]
# Sat, 24 Jun 2023 02:31:26 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 02:31:41 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 24 Jun 2023 02:31:42 GMT
USER ContainerUser
# Sat, 24 Jun 2023 02:52:25 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Sat, 24 Jun 2023 02:57:37 GMT
ENV MONGO_VERSION=4.4.22
# Sat, 24 Jun 2023 02:58:01 GMT
COPY dir:ba7da3b127dd995e6b5f5a8e9cc5f87caa3174d8a03e6b82fdeaa7d4f4b54ce8 in C:\mongodb 
# Sat, 24 Jun 2023 02:58:17 GMT
RUN mongo --version && mongod --version
# Sat, 24 Jun 2023 02:58:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:58:18 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:58:19 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:d6e77b89ecdadfdd3ef274e9a235590c9cd4dc832939932eff32f93250571005`  
		Last Modified: Fri, 23 Jun 2023 07:43:32 GMT  
		Size: 120.0 MB (120028254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b2deb8649e4dedd9fbe74195175cfdae8176065d0daa61337779d26f0bce93`  
		Last Modified: Sat, 24 Jun 2023 02:17:36 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c851c15426494687424d4597399ac88799abfe339928d85f4df7a6abdbed5ffc`  
		Last Modified: Sat, 24 Jun 2023 06:32:16 GMT  
		Size: 1.2 KB (1168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9545ffe158e5ffac274b8e7c5297117a1f8983e3a4e95d6a8baffe412d1b51ef`  
		Last Modified: Sat, 24 Jun 2023 06:32:14 GMT  
		Size: 80.6 KB (80567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c836921d67898e578c9bc0af8cd07ff59136154efb53925baca8c19bed341989`  
		Last Modified: Sat, 24 Jun 2023 06:32:14 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71a1f9cf9505113f36b7171be921a9786923b3da255d62cb98bdbb5967c4c290`  
		Last Modified: Sat, 24 Jun 2023 06:49:22 GMT  
		Size: 263.5 KB (263506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38dd09c0040ab39259201b3f39f5fe3ab917a2ef07cfa483c10783a80717d5bf`  
		Last Modified: Sat, 24 Jun 2023 06:53:19 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:638e5591939d1123fbc3d92a95d96fa2f0301d89c7421ce1745d94b75d7748ca`  
		Last Modified: Sat, 24 Jun 2023 06:53:58 GMT  
		Size: 245.0 MB (245043192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95111273a4dc283ac5ad5d2d7cdeeaf528df97bf91ca8b4263f9f9c153257587`  
		Last Modified: Sat, 24 Jun 2023 06:53:17 GMT  
		Size: 57.1 KB (57060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b9fef2169a847116ef5632af61e6d00d859bf8696f750c78fd42b0b82b58bb9`  
		Last Modified: Sat, 24 Jun 2023 06:53:17 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70f89329b653520c045a0bac955fb5ffebef460d31687782b88054ae83af8a0e`  
		Last Modified: Sat, 24 Jun 2023 06:53:17 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:312e46ccac653b7b2ca10c71640db527d034dba0fdafff44b8acd508a9097138`  
		Last Modified: Sat, 24 Jun 2023 06:53:17 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:7240020e2865a9ac35ae3669827789393fa35513a246822abaeddf31153c5f8c
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.9 MB (349875041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09820470ec8f997792b8ffa719b566e251721975eca74038fc25301aa50724b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 01:50:24 GMT
SHELL [cmd /S /C]
# Sat, 24 Jun 2023 02:33:09 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 02:33:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 24 Jun 2023 02:33:24 GMT
USER ContainerUser
# Sat, 24 Jun 2023 02:53:18 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Sat, 24 Jun 2023 02:58:30 GMT
ENV MONGO_VERSION=4.4.22
# Sat, 24 Jun 2023 02:58:50 GMT
COPY dir:ba7da3b127dd995e6b5f5a8e9cc5f87caa3174d8a03e6b82fdeaa7d4f4b54ce8 in C:\mongodb 
# Sat, 24 Jun 2023 02:59:03 GMT
RUN mongo --version && mongod --version
# Sat, 24 Jun 2023 02:59:04 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:59:05 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:59:06 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0712dde7e721d063ebcbe80a9968c96e3b3af1f54a33928786e0d37335da4cd`  
		Last Modified: Sat, 24 Jun 2023 02:18:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a638f113f886e54e8e494347981d25a36f28873f1b9e0905cef7ef9ef0227`  
		Last Modified: Sat, 24 Jun 2023 06:33:56 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4deb983b7c23277ea52231f8a02797b91fd72aad7b9b8234cceb857505961`  
		Last Modified: Sat, 24 Jun 2023 06:33:54 GMT  
		Size: 69.6 KB (69575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3592f8eaf22ebd67118459d39e793af2168190561abf11f80b1f570fb5a468f9`  
		Last Modified: Sat, 24 Jun 2023 06:33:54 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa83bb255dac1342d46c74b00ab672aa77772aecbd463ea10848b3db8c2257f`  
		Last Modified: Sat, 24 Jun 2023 06:50:26 GMT  
		Size: 263.5 KB (263520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383f34a0e20a9841492a6888efa1f63c5266eaba230b6d88ec6ffcb842789bf8`  
		Last Modified: Sat, 24 Jun 2023 06:54:11 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df9b86fe145eda3b00fafc69abd9f43272569642b9aa1fff662376cd70aaae3f`  
		Last Modified: Sat, 24 Jun 2023 06:54:51 GMT  
		Size: 245.0 MB (245044707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872de1ad9fff8ebab15f5cffa1c496a9bbb211993847e13d7504e32dea9cc9be`  
		Last Modified: Sat, 24 Jun 2023 06:54:09 GMT  
		Size: 88.2 KB (88202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d032c444d04d2f6ccc543194b9dbab529fb581b719e30605d4061f01e4c36b63`  
		Last Modified: Sat, 24 Jun 2023 06:54:09 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68d99cb2f750f7982c6fd53686fe0468faf2358e2239e7d222e708363638f128`  
		Last Modified: Sat, 24 Jun 2023 06:54:09 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1e4e477bfa86004fb3aa2a96650330ed44bf69ebdc281b833b5a8c9e98a03d4`  
		Last Modified: Sat, 24 Jun 2023 06:54:09 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
