## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:655d1bd7314577671ea44b76494da9ef3af7a91dae80584bf2f14513c62f6b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.1249; amd64
	-	windows version 10.0.17763.3650; amd64

### `mongo:5-nanoserver` - windows version 10.0.20348.1249; amd64

```console
$ docker pull mongo@sha256:a3cdb3d1caf784a55593ac38c0113f1610c08f8534b0b9a6c7e8224d6bc468ce
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **432.2 MB (432191899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42c9ac2479b7e1cb489fe687fbd22a407f41d1518f4dd3b2cb3a61781c67648b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Nov 2022 07:21:30 GMT
RUN Apply image 10.0.20348.1249
# Wed, 09 Nov 2022 14:03:51 GMT
SHELL [cmd /S /C]
# Wed, 09 Nov 2022 18:28:15 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 18:28:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Nov 2022 18:28:36 GMT
USER ContainerUser
# Wed, 09 Nov 2022 18:36:29 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 22 Nov 2022 23:24:14 GMT
ENV MONGO_VERSION=5.0.14
# Tue, 22 Nov 2022 23:24:55 GMT
COPY dir:e35592cc21ade3cccd2a05122103ef64998dd68366a249105c90037f275f3b5b in C:\mongodb 
# Tue, 22 Nov 2022 23:25:19 GMT
RUN mongo --version && mongod --version
# Tue, 22 Nov 2022 23:25:20 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 22 Nov 2022 23:25:21 GMT
EXPOSE 27017
# Tue, 22 Nov 2022 23:25:22 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:72e5d750fe8c1a32d4a26ef3b4a4e1f6124ac079b142f12724af2abfcba1c8b3`  
		Last Modified: Tue, 08 Nov 2022 19:57:58 GMT  
		Size: 122.1 MB (122092167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5798382a92edbf13363f09d29194b10dba5ce50456d5499d8b33a42e2c702cd`  
		Last Modified: Wed, 09 Nov 2022 14:34:17 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9fa4dc6ee264fdf67c57b4158cf6e575cb0a820aa5dbb991e3f333d2202307b`  
		Last Modified: Wed, 09 Nov 2022 19:06:19 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980b091f06a8d628071da46b850437b7a38c09046802ff108c9aff1d62451525`  
		Last Modified: Wed, 09 Nov 2022 19:06:16 GMT  
		Size: 86.9 KB (86878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be0725d6d4e52a7894c3c2a870fd0f22b94e68d055eae2cc57a75b9b41ea6318`  
		Last Modified: Wed, 09 Nov 2022 19:06:16 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aefabfbbe03c334aba82e08dee17043a6c00406655e5fc13a72554e0ae7b4cfc`  
		Last Modified: Wed, 09 Nov 2022 19:12:12 GMT  
		Size: 263.5 KB (263495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41f09d02fb237dc63d29e1728247704050458bfa678dd1d98d46b9bddec617c9`  
		Last Modified: Wed, 23 Nov 2022 00:20:53 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4e8a20ed025c08d333203a00214667060d91bb78bed4390ee248010634d993`  
		Last Modified: Wed, 23 Nov 2022 00:21:47 GMT  
		Size: 309.7 MB (309692081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5bd07ec3db8d7c79ca3a9f87194f0819d75fc1c35d17f0402bf0c8a3b29748`  
		Last Modified: Wed, 23 Nov 2022 00:20:50 GMT  
		Size: 49.2 KB (49166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b102b7c5ccff007b339fb5e71bd2b8f92e6237e2441e32ae7db90dafc835393e`  
		Last Modified: Wed, 23 Nov 2022 00:20:50 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c42468781bcdd394a572914d7bf5217360fb69fe0645aeb0fb39f249c20f604`  
		Last Modified: Wed, 23 Nov 2022 00:20:50 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ceff9d90516114ec51cf9c1e2c6f9b46fbbad03a265040e045689391876d23`  
		Last Modified: Wed, 23 Nov 2022 00:20:50 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:5-nanoserver` - windows version 10.0.17763.3650; amd64

```console
$ docker pull mongo@sha256:d8aafd71eaf8c03a5039074f083f8103253f5fd46aabc42bd5e984788ed2f42e
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.8 MB (416837065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b08b17ef4c08ac184fd08c9b78c853c08b338140b5e6eeef51a5351455f99b2b`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 05 Nov 2022 18:06:28 GMT
RUN Apply image 10.0.17763.3650
# Wed, 09 Nov 2022 14:09:15 GMT
SHELL [cmd /S /C]
# Wed, 09 Nov 2022 18:30:00 GMT
USER ContainerAdministrator
# Wed, 09 Nov 2022 18:30:15 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 09 Nov 2022 18:30:16 GMT
USER ContainerUser
# Wed, 09 Nov 2022 18:37:49 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Tue, 22 Nov 2022 23:25:44 GMT
ENV MONGO_VERSION=5.0.14
# Tue, 22 Nov 2022 23:26:27 GMT
COPY dir:e35592cc21ade3cccd2a05122103ef64998dd68366a249105c90037f275f3b5b in C:\mongodb 
# Tue, 22 Nov 2022 23:27:05 GMT
RUN mongo --version && mongod --version
# Tue, 22 Nov 2022 23:27:06 GMT
VOLUME [C:\data\db C:\data\configdb]
# Tue, 22 Nov 2022 23:27:07 GMT
EXPOSE 27017
# Tue, 22 Nov 2022 23:27:08 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:35ab4104a4d9df6a0d1eac84cc8fbc13511ef6c8aef5ced04fdf63e7e20803a3`  
		Last Modified: Tue, 08 Nov 2022 19:45:20 GMT  
		Size: 106.7 MB (106723592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a83e42a06a19f2d133476fa58d61bf56ed65a782146e4f8b37b3fc8727440fbd`  
		Last Modified: Wed, 09 Nov 2022 14:35:26 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6449712c858131bae1c7bddbe1897bb48c821a1169952834ef9364fee0384db`  
		Last Modified: Wed, 09 Nov 2022 19:08:05 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e914de04c2af4eb226e2cb7b4bbcf383cb62175d5df12dbcc9b03bba182e41`  
		Last Modified: Wed, 09 Nov 2022 19:08:02 GMT  
		Size: 71.4 KB (71358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca05487e297333fc707a0a3c04d76f9c45b34ab868772e71f7eebbd106664df`  
		Last Modified: Wed, 09 Nov 2022 19:08:02 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635580a42bba22cbe74bf589efb5ed78d794665d909c36216aea3d718da59b7e`  
		Last Modified: Wed, 09 Nov 2022 19:13:23 GMT  
		Size: 263.5 KB (263460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22b41470fbdbf7abbd36f2379eb0ebd30bcaa60b2fa4d37ccfc861bf5162b3f8`  
		Last Modified: Wed, 23 Nov 2022 00:22:00 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbf73e21190a020133dfce5e45ef2f2c6860fcf26ab3ec9f2c530060e53887b0`  
		Last Modified: Wed, 23 Nov 2022 00:22:53 GMT  
		Size: 309.7 MB (309692102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da7bcf55f1ea673489efd503f49d018d54dcfd701851798303c2d072dec77ef`  
		Last Modified: Wed, 23 Nov 2022 00:21:58 GMT  
		Size: 78.5 KB (78519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f054a25eb87cbec31f00eabc5b9de93d2809f12e4393dc77f495944663ea1d6`  
		Last Modified: Wed, 23 Nov 2022 00:21:57 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:894024beb6e60e5977b7ae1a1aca140c7ac6f919c355e730420ae63624db07a6`  
		Last Modified: Wed, 23 Nov 2022 00:21:57 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:323639eb5119e21751472bc77ae8f56b6e7eb8ee251c60b48f6a85a7f975fc7e`  
		Last Modified: Wed, 23 Nov 2022 00:21:57 GMT  
		Size: 1.1 KB (1114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
