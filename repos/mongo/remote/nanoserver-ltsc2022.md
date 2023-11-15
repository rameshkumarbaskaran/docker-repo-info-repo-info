## `mongo:nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:edf097591a91e71e05f3104e21384fbb8c1afb08a70421a25f707b2ba9a01384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.2031; amd64

### `mongo:nanoserver-ltsc2022` - windows version 10.0.20348.2031; amd64

```console
$ docker pull mongo@sha256:ee99e53ed690b19bf41095efd3d73c47373ad17df402e0e8dd85a7b938a52693
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.2 MB (732225876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b1a05d9fa1563e13c61bb409e5438e6e38f64c30b1f8b42c3e6e52292dd0c4`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Fri, 06 Oct 2023 21:30:39 GMT
RUN Apply image 10.0.20348.2031
# Wed, 11 Oct 2023 02:28:41 GMT
SHELL [cmd /S /C]
# Wed, 11 Oct 2023 03:03:40 GMT
USER ContainerAdministrator
# Wed, 11 Oct 2023 03:04:28 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 11 Oct 2023 03:04:29 GMT
USER ContainerUser
# Wed, 11 Oct 2023 03:04:30 GMT
COPY multi:4abffac378fdd7fd5082d54935b2f9dc2024a93fc9837ae8701ac6e024ef02ee in C:\Windows\System32\ 
# Wed, 15 Nov 2023 02:32:34 GMT
ENV MONGO_VERSION=7.0.3
# Wed, 15 Nov 2023 02:33:24 GMT
COPY dir:7eb07008f9caa03d65261324d8b15c9bab0915a192363e36e5cb23930a2b52b0 in C:\mongodb 
# Wed, 15 Nov 2023 02:33:44 GMT
RUN mongod --version
# Wed, 15 Nov 2023 02:33:45 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 15 Nov 2023 02:33:46 GMT
EXPOSE 27017
# Wed, 15 Nov 2023 02:33:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:fff54800e03713ba81736f43d985319592fc643a1a32b62dbd5c0ec36549de00`  
		Last Modified: Tue, 10 Oct 2023 17:30:43 GMT  
		Size: 120.6 MB (120604344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54cd425f94dc5addd6f49003c495c9acbf2a61ab29ca68946c6cd056ed33c5f6`  
		Last Modified: Wed, 11 Oct 2023 02:48:05 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c5d8a4d1b8dd712544f618c2e6ee6be0146ea27a9e28326d8d91f8bd6fa8a0`  
		Last Modified: Wed, 11 Oct 2023 07:41:29 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2c9710a873f77c9b8cdf8f8359453db5ea2693415cdcd182e0478772b06b5f`  
		Last Modified: Wed, 11 Oct 2023 07:41:28 GMT  
		Size: 87.1 KB (87090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e705c53faad5aaf4367e374cfed21b9e0b718d308280d68adb51337227f65b`  
		Last Modified: Wed, 11 Oct 2023 07:41:27 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9d5b2d3c7888d6f3686a12fd05ea8addf1740213bcf2aea7dfd0a6000b8d5e1`  
		Last Modified: Wed, 11 Oct 2023 07:41:28 GMT  
		Size: 267.2 KB (267168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea86a194d93d5b21f2c4f4da354e9ac52fc0d357ef189cc783d4e9fa50f389e`  
		Last Modified: Wed, 15 Nov 2023 03:14:57 GMT  
		Size: 1.2 KB (1174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fedd104eebbd9e9c9fb32bd45776de5cf1a0acac33683d4a86244ca97b5c77f8`  
		Last Modified: Wed, 15 Nov 2023 03:17:00 GMT  
		Size: 611.2 MB (611209135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e63767cdeb77c54e451418b5c10c37af69106414d4029291a7b865025db3d9d`  
		Last Modified: Wed, 15 Nov 2023 03:14:55 GMT  
		Size: 50.0 KB (50031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b94f6bfc33994749af44f28334ccf472601c1f4b3f4732c25945c3bb3e9f30`  
		Last Modified: Wed, 15 Nov 2023 03:14:55 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eed4049641c34b08cb2ccbdf55290741024180c7947be8ba84fce63d7c8affe0`  
		Last Modified: Wed, 15 Nov 2023 03:14:55 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63afd3c321e9f7bdcdad93145a55ab329bc4e173be0dd82a22492a5f309b987`  
		Last Modified: Wed, 15 Nov 2023 03:14:55 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
