## `mongo:4-nanoserver-1809`

```console
$ docker pull mongo@sha256:03e57d262df99a4172a3f3d5b0a2bb389b469df1ff314446e3c0f64b70f49c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2803; amd64

### `mongo:4-nanoserver-1809` - windows version 10.0.17763.2803; amd64

```console
$ docker pull mongo@sha256:54188ae92b5da9e8b212fe8f90eb2a244a9f2cd05c3897db5ccc10de141f0142
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.1 MB (345107623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa83c4e50de9d72b7423ffba0f7a483dae99ec656984b47ce9920cac1f9d967c`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Mon, 04 Apr 2022 10:52:49 GMT
RUN Apply image 1809-amd64
# Wed, 13 Apr 2022 02:48:06 GMT
SHELL [cmd /S /C]
# Wed, 13 Apr 2022 17:35:28 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:35:35 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Apr 2022 17:35:36 GMT
USER ContainerUser
# Wed, 13 Apr 2022 17:35:38 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 13 Apr 2022 17:41:11 GMT
ENV MONGO_VERSION=4.4.13
# Wed, 13 Apr 2022 17:41:34 GMT
COPY dir:cb2795f5b405c92d2e3366f5e962d386ae580b206db49ff53e53730c9b68815c in C:\mongodb 
# Wed, 13 Apr 2022 17:41:41 GMT
RUN mongo --version && mongod --version
# Wed, 13 Apr 2022 17:41:42 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:41:42 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:41:43 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:6fc97003d8b7f593fe071cf3ea64f3ce760cc060f3402bb6b1b849c040e222d5`  
		Size: 103.1 MB (103096169 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:a1e4f80cd1f664faa50444f6850501c0035534cf86f2ed0b458586b9f4b5089e`  
		Last Modified: Wed, 13 Apr 2022 03:18:01 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19568f22509c76cadae091bbc3a9c4064c4d0c458b1c66b01af3820fe0d3f5e`  
		Last Modified: Wed, 13 Apr 2022 18:06:51 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:686e0047ea9d2b545c4705a478cf3f5a8ba67594255da0a0794a75bdbd829339`  
		Last Modified: Wed, 13 Apr 2022 18:06:49 GMT  
		Size: 70.3 KB (70348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc7042f8e1bb874fc050093e4073fc53cbfc0e7ac47c18a5c163f5c541181c96`  
		Last Modified: Wed, 13 Apr 2022 18:06:48 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14043e3c2c29d92551a552ccde6c8c9ca4a27a12b67eb4d95b9a99ff3cea0088`  
		Last Modified: Wed, 13 Apr 2022 18:06:49 GMT  
		Size: 263.5 KB (263523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ea40c3126b5500fd01a6efa4d699ad72cb9d473a9b1ae2e2311c64414cc5afd`  
		Last Modified: Wed, 13 Apr 2022 18:23:02 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:960b7461d989c1cb1c5e115bc5ab28b1427e88d75fe3b4a4d2bcaf481f47eb76`  
		Last Modified: Wed, 13 Apr 2022 18:27:40 GMT  
		Size: 241.6 MB (241620446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f95da4a2a7264403192ce6fc810fa80af4fe7256c029948025b74c9f1ee204`  
		Last Modified: Wed, 13 Apr 2022 18:23:00 GMT  
		Size: 49.2 KB (49190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:756e5f1e0e85d695251090ca326bfe637b66d3c5e3c5a4b5d8ef071f17a55e41`  
		Last Modified: Wed, 13 Apr 2022 18:23:00 GMT  
		Size: 1.1 KB (1118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bc2edfd7e1bf056674dd12e16df06aab9ba9e27ea662284b5c4f2723ae19f6f`  
		Last Modified: Wed, 13 Apr 2022 18:23:00 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9643bcb44bd78f50f5c5ba964f940c798f64be3a1ad97ce25132e90deded9775`  
		Last Modified: Wed, 13 Apr 2022 18:23:00 GMT  
		Size: 1.1 KB (1119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
