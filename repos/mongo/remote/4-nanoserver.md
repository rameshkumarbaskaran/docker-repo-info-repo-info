## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:481d12947fd72675b14a74b38b66c58e78a8a20e2022fbc0b6edb0c88c76c6ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.2159; amd64
	-	windows version 10.0.17763.5206; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.2159; amd64

```console
$ docker pull mongo@sha256:63a894c08a5daaa1622624543264ab72bc1c748e358c7b9d489707386c8a2da7
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365610919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52af35c14a2319e704a829a83859cf4cd212777d199a0cf01ab0c97b05c182c0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sat, 02 Dec 2023 12:14:23 GMT
RUN Apply image 10.0.20348.2159
# Sat, 16 Dec 2023 00:01:27 GMT
SHELL [cmd /S /C]
# Sat, 16 Dec 2023 00:01:27 GMT
USER ContainerAdministrator
# Sat, 16 Dec 2023 00:01:30 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 16 Dec 2023 00:01:31 GMT
USER ContainerUser
# Sat, 16 Dec 2023 00:01:32 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Sat, 16 Dec 2023 00:01:33 GMT
ENV MONGO_VERSION=4.4.26
# Sat, 16 Dec 2023 00:01:46 GMT
COPY dir:c0f16ed64e5cc45756102556aceda7ef6f4d8710826a691604a4606895f46575 in C:\mongodb 
# Sat, 16 Dec 2023 00:01:55 GMT
RUN mongo --version && mongod --version
# Sat, 16 Dec 2023 00:01:56 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 16 Dec 2023 00:01:57 GMT
EXPOSE 27017
# Sat, 16 Dec 2023 00:01:57 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:075332bb10f7fc70c56f7c073dd753e05cacbc93a38c181c5576739a29f8a7e1`  
		Last Modified: Tue, 12 Dec 2023 21:35:16 GMT  
		Size: 120.8 MB (120757041 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7042cc9bfb224c5d969725e5dc996c34eed418403fc15c67fa6adda3b9b793`  
		Last Modified: Sat, 16 Dec 2023 00:02:02 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c617bab92975944356740dc61ba41176b9f97e41a0f981cbabb8aad8cb9187a8`  
		Last Modified: Sat, 16 Dec 2023 00:02:02 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19bdf37cd22881f8a660589b0f8dadfeea6c8a925866d3253aede7fdb64f1462`  
		Last Modified: Sat, 16 Dec 2023 00:02:01 GMT  
		Size: 78.8 KB (78807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f53b3c1122be1c483696ea42ffe25f6e9f631783e5985501060b2afa84c766f`  
		Last Modified: Sat, 16 Dec 2023 00:02:01 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a823a56bcb1ae66a37bbefe95948f3edd9af8c1ce8cd3f323c044647afda6786`  
		Last Modified: Sat, 16 Dec 2023 00:02:01 GMT  
		Size: 263.5 KB (263468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:730a83e39c75cef9a364f9acbdcfe336120fe52fd9a48fa69d687217dc4d317c`  
		Last Modified: Sat, 16 Dec 2023 00:02:01 GMT  
		Size: 1.1 KB (1112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7574c1aa3269a56a5587fd7ad970b43994705aaa0ec3ff30aea40aaf4afe7b45`  
		Last Modified: Sat, 16 Dec 2023 00:02:24 GMT  
		Size: 244.4 MB (244411199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9c956c1dea05bd3ad7d40b65581e470cb1f30e6dfb4c7e8b5673f12915962d1`  
		Last Modified: Sat, 16 Dec 2023 00:02:00 GMT  
		Size: 93.0 KB (92991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7766d5756c3c36fb14790c597330fd49ee2fc9d2c31215af49a2feb520ece9`  
		Last Modified: Sat, 16 Dec 2023 00:02:00 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c618e9be84a1599b11b6026bf9268195e2ac322a5e67282208cb75353ef496d1`  
		Last Modified: Sat, 16 Dec 2023 00:02:00 GMT  
		Size: 1.1 KB (1078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d37c6eda7e31c4105c61369a6e5bebe3914738acbcc9047fc8d09fd9b0f6f99c`  
		Last Modified: Sat, 16 Dec 2023 00:02:00 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.5206; amd64

```console
$ docker pull mongo@sha256:bf6b621082d860dd4c9b1747532a7a5cef4cd7b21a361ed020c84fc0ce087f81
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **349.3 MB (349349790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c75c86984669233c8d8d759f75f6b2bda0e68c53ac594290e72e7f957835ce5f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Fri, 15 Dec 2023 23:57:15 GMT
SHELL [cmd /S /C]
# Fri, 15 Dec 2023 23:57:16 GMT
USER ContainerAdministrator
# Fri, 15 Dec 2023 23:57:17 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Fri, 15 Dec 2023 23:57:18 GMT
USER ContainerUser
# Fri, 15 Dec 2023 23:57:19 GMT
COPY multi:d83167ee7f0a01f519841410f1f031c3bdfa566af08cc1936efaf3b3f20e2b0f in C:\Windows\System32\ 
# Fri, 15 Dec 2023 23:57:19 GMT
ENV MONGO_VERSION=4.4.26
# Fri, 15 Dec 2023 23:57:34 GMT
COPY dir:c0f16ed64e5cc45756102556aceda7ef6f4d8710826a691604a4606895f46575 in C:\mongodb 
# Fri, 15 Dec 2023 23:57:39 GMT
RUN mongo --version && mongod --version
# Fri, 15 Dec 2023 23:57:40 GMT
VOLUME [C:\data\db C:\data\configdb]
# Fri, 15 Dec 2023 23:57:41 GMT
EXPOSE 27017
# Fri, 15 Dec 2023 23:57:42 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642a06b62e585bd242dc073e7df843b3b400a6f1c59c937463956cb0249bf36`  
		Last Modified: Fri, 15 Dec 2023 23:57:50 GMT  
		Size: 1.0 KB (1039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:836510469b5abef2068e4eea7a5794f367de62a00af745386aaf7571c7e9efb2`  
		Last Modified: Fri, 15 Dec 2023 23:57:50 GMT  
		Size: 1.1 KB (1051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0870f33aa96b4e6493ef8be2051d4a77aa0d708e9a363f410fc87712be99ff76`  
		Last Modified: Fri, 15 Dec 2023 23:57:48 GMT  
		Size: 71.2 KB (71181 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12342fa195ebe7d8d5dbea82d8da83b7cbd5423b101bfeac3a9730f7cd933f70`  
		Last Modified: Fri, 15 Dec 2023 23:57:48 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04fc19e75b5c6d642672af723953400b93abd9085ad425333a63c9cb9f0979f4`  
		Last Modified: Fri, 15 Dec 2023 23:57:48 GMT  
		Size: 263.4 KB (263379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7357d09eb0e793f928cf2f73bd917b12d1d5ad766048c18e24d20ea3c79fd6fd`  
		Last Modified: Fri, 15 Dec 2023 23:57:47 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0243be2f470f27a653027f8177cb0f10778b4b7de051a24a4af457753898516b`  
		Last Modified: Fri, 15 Dec 2023 23:58:10 GMT  
		Size: 244.4 MB (244411061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2270478e70f06667fe38d57ef5bf0a852d906e588157ff09a88c2c4fd39f075`  
		Last Modified: Fri, 15 Dec 2023 23:57:46 GMT  
		Size: 86.7 KB (86705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39eb878d81d0ea02a17bc886a8611134ac6ce9835006f6468134ad7b63a65a43`  
		Last Modified: Fri, 15 Dec 2023 23:57:45 GMT  
		Size: 1.0 KB (1036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba6acca2e4124b5c79d184d96c4486c94dab1c23c0ef20a85ae25060d287d61f`  
		Last Modified: Fri, 15 Dec 2023 23:57:46 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00c565ebec87342fb1833a364bf157a88cd51acdc3e4949fe825ab2495db6d2`  
		Last Modified: Fri, 15 Dec 2023 23:57:46 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
