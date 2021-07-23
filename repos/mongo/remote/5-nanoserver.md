## `mongo:5-nanoserver`

```console
$ docker pull mongo@sha256:fdc4c1fc53e5fb40e6080a87c13bd882aa41001e89ae3781200b724acc518880
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2061; amd64

### `mongo:5-nanoserver` - windows version 10.0.17763.2061; amd64

```console
$ docker pull mongo@sha256:422bd486d5ef1da2fee50edc2c9612758d7b8b86bd056c64338d42637fd461c7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.4 MB (392430965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f0e8481d37a7c1c01c07c05198cefc30e30a48ed6eb44ef5d11bf8691aad9ec`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 06 Jul 2021 20:06:39 GMT
RUN Apply image 1809-amd64
# Wed, 14 Jul 2021 01:23:41 GMT
SHELL [cmd /S /C]
# Wed, 14 Jul 2021 01:23:44 GMT
USER ContainerAdministrator
# Wed, 14 Jul 2021 01:24:39 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Wed, 14 Jul 2021 01:24:40 GMT
USER ContainerUser
# Wed, 14 Jul 2021 01:24:44 GMT
COPY multi:0196f9e96f60ad3e2b92fd0773f8d0fe3a8235e1eefbb9ef1a1f0d672e6a711c in C:\Windows\System32\ 
# Thu, 22 Jul 2021 22:22:33 GMT
ENV MONGO_VERSION=5.0.1
# Thu, 22 Jul 2021 22:23:04 GMT
COPY dir:cbdbd002f51906538fd2f684695a4a11dc584c8648de8d7f35d80ace109e59c7 in C:\mongodb 
# Thu, 22 Jul 2021 22:23:39 GMT
RUN mongo --version && mongod --version
# Thu, 22 Jul 2021 22:23:41 GMT
VOLUME [C:\data\db C:\data\configdb]
# Thu, 22 Jul 2021 22:23:44 GMT
EXPOSE 27017
# Thu, 22 Jul 2021 22:23:46 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:29d43e56445c5279a6386c4dfe4d1ada3c7124ade9cb7b0f2757e58ffc7cd10b`  
		Size: 102.7 MB (102725622 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5307d56ac81f33a647e0ed6f4e0f70a39b207469fe0a28ab1b9f9379669e02b4`  
		Last Modified: Wed, 14 Jul 2021 02:04:59 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a611bf59a988b0a5edd06e25ae07583657165333b55f3f7591f225964532c294`  
		Last Modified: Wed, 14 Jul 2021 02:04:59 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e35563eb5bf880fe10ab1cac2d96621bb2821366f761cb76ab30d8bb3aa1463`  
		Last Modified: Wed, 14 Jul 2021 02:04:57 GMT  
		Size: 66.6 KB (66629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b09241ae500a15f03f3c5e117bcfa73142ca23eafad6e31850d18aae5d11779`  
		Last Modified: Wed, 14 Jul 2021 02:04:56 GMT  
		Size: 1.1 KB (1105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc5c146eb6617702bbcff62dc5eec3d43581bd5388fb1c2a75c9d69a7ac66470`  
		Last Modified: Wed, 14 Jul 2021 02:04:56 GMT  
		Size: 274.0 KB (274011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9ca939187729606f97e3d0009853949c4a4c4d28c4686b24bc77751fe2cbba7`  
		Last Modified: Thu, 22 Jul 2021 22:28:39 GMT  
		Size: 1.1 KB (1090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6243defcd4047fd11d515151a3b3fd5c4fa6fed3f2d0e3791a61efbf302ff1f1`  
		Last Modified: Thu, 22 Jul 2021 22:29:28 GMT  
		Size: 289.3 MB (289288422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5ff919697095d56ff6b365dc1b9bb1638acd0b8a90d2c053f822d254baca9d`  
		Last Modified: Thu, 22 Jul 2021 22:28:41 GMT  
		Size: 68.5 KB (68521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0ce77d524aa8e1d5c54423d66b972d394ecb159ccf07e5e177066b9b16b4a54`  
		Last Modified: Thu, 22 Jul 2021 22:28:36 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235bb25ee8a476b968ec1cb247937c64b0d61618ce82732c0e4b1041ad0d85f7`  
		Last Modified: Thu, 22 Jul 2021 22:28:36 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca43eb67a69cb72890fb5f672b24b8de347471b0a9e0f658e6c1e823784d00d2`  
		Last Modified: Thu, 22 Jul 2021 22:28:36 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
