## `mongo:nanoserver`

```console
$ docker pull mongo@sha256:3797ba5b9e9aa30fcc0f42358d7f8dd96aca80e1a4433ea79e1af98b570bf5cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.643; amd64
	-	windows version 10.0.17763.2803; amd64

### `mongo:nanoserver` - windows version 10.0.20348.643; amd64

```console
$ docker pull mongo@sha256:5534f1f8cbe18970bbe532072a5a745434c50654ab0942a08fb2a7e33ed30f15
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **423.6 MB (423581915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84d58b08e3fa869d55f12d839b38025bc1c182868d93fc63fb89478b8f4c449a`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 03 Apr 2022 05:29:07 GMT
RUN Apply image ltsc2022-amd64
# Wed, 13 Apr 2022 02:43:38 GMT
SHELL [cmd /S /C]
# Wed, 13 Apr 2022 17:34:27 GMT
USER ContainerAdministrator
# Wed, 13 Apr 2022 17:34:36 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 13 Apr 2022 17:34:37 GMT
USER ContainerUser
# Wed, 13 Apr 2022 17:34:38 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Wed, 13 Apr 2022 17:34:39 GMT
ENV MONGO_VERSION=5.0.7
# Wed, 13 Apr 2022 17:35:08 GMT
COPY dir:fb35459f874a32c339bad763a07251484cc13f01f904e8d607c367bab2629f9a in C:\mongodb 
# Wed, 13 Apr 2022 17:35:16 GMT
RUN mongo --version && mongod --version
# Wed, 13 Apr 2022 17:35:17 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:35:17 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:35:18 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:5ee98801bdad72bc36678d072c89f7dd482fee29086c1d9c8ad6ff0cb5afa385`  
		Size: 117.6 MB (117579416 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0ae7f8fcefe8f9cd0745bf20258e1950e1c72b8ca86cc031fca90ec3e24203e`  
		Last Modified: Wed, 13 Apr 2022 03:16:38 GMT  
		Size: 1.1 KB (1133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08f6eb35034542f1e8cda3b15fc48faf88551e753d68db2a9567d62a8b2f4139`  
		Last Modified: Wed, 13 Apr 2022 18:01:19 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a897233ecb418719699d59c61a5a680dba34aed5b55156109835b7c7979972`  
		Last Modified: Wed, 13 Apr 2022 18:01:17 GMT  
		Size: 87.6 KB (87595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222eec50270ee0d80f5d695a57ac3acb77fcfa12b827d5b72852aef4e28990bd`  
		Last Modified: Wed, 13 Apr 2022 18:01:16 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d0e50b581be23686aad76397f0b3d3325837a54885da2740b7414e7de1ceb79`  
		Last Modified: Wed, 13 Apr 2022 18:01:17 GMT  
		Size: 263.4 KB (263435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2008c30a424f74aeeaf97d825e04905efe1ab87b3108b2cef1bf00d6e3d284f`  
		Last Modified: Wed, 13 Apr 2022 18:01:17 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108b190ac4e44939058a18e9aeb679b8dbe210f47832c5f4a801bbbbf11798bb`  
		Last Modified: Wed, 13 Apr 2022 18:06:28 GMT  
		Size: 305.6 MB (305594019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07f03c3c047f462a89bb6c835006d98381da2887c61404fbe849916bfba928a`  
		Last Modified: Wed, 13 Apr 2022 18:01:14 GMT  
		Size: 49.4 KB (49368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcba02be9d3e52a6ed74e19098663b8f77ba242f99b808982f6bae598054e042`  
		Last Modified: Wed, 13 Apr 2022 18:01:14 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e17084e46ada904f877b66bff7e99740d77de0e935422fa4a4133b254dad6752`  
		Last Modified: Wed, 13 Apr 2022 18:01:14 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0c0de5d2645440d5949592f8c6115abaa9c893f6d635791085a1eae5ceff791`  
		Last Modified: Wed, 13 Apr 2022 18:01:14 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:nanoserver` - windows version 10.0.17763.2803; amd64

```console
$ docker pull mongo@sha256:3189fc1a2548707914c4b1d1af2a3894d356514383e9169839cd7b01e4d8a7d9
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **409.1 MB (409081545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bb9104dd259b2ae0da5b0972f6748777ac3dd3a2dc7657b745256642e7293b`
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
# Wed, 13 Apr 2022 17:35:39 GMT
ENV MONGO_VERSION=5.0.7
# Wed, 13 Apr 2022 17:36:06 GMT
COPY dir:fb35459f874a32c339bad763a07251484cc13f01f904e8d607c367bab2629f9a in C:\mongodb 
# Wed, 13 Apr 2022 17:36:13 GMT
RUN mongo --version && mongod --version
# Wed, 13 Apr 2022 17:36:14 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 13 Apr 2022 17:36:15 GMT
EXPOSE 27017
# Wed, 13 Apr 2022 17:36:16 GMT
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
	-	`sha256:f8f1a418c1ee31f7bb007de0d6cb464cafb8623887186af1b5d1108bd892ecf8`  
		Last Modified: Wed, 13 Apr 2022 18:06:48 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:355335411c814030e52539f358056f9038aa403b7898647e7bf00a419f7b54fe`  
		Last Modified: Wed, 13 Apr 2022 18:12:19 GMT  
		Size: 305.6 MB (305593993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34d74faff7ae4fd03e3431fa8443b9751421072e79d4f52c16db5214cbce2f07`  
		Last Modified: Wed, 13 Apr 2022 18:06:46 GMT  
		Size: 49.5 KB (49541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3af9313ffda1c2acfe1a9c21088977115c039f2cd54e36371914d12e5d6b3201`  
		Last Modified: Wed, 13 Apr 2022 18:06:46 GMT  
		Size: 1.1 KB (1140 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1343bdd126a19b7b7679bbf475af2dc88815c0f6a74442d9f9f79b0a76cd3d4b`  
		Last Modified: Wed, 13 Apr 2022 18:06:46 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55da370dc0d6a98f55242b631e5eefa6bc04dd632eb59027c1e41cd51e13aff6`  
		Last Modified: Wed, 13 Apr 2022 18:06:46 GMT  
		Size: 1.1 KB (1139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
