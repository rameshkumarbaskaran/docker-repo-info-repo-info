## `mongo:4-nanoserver`

```console
$ docker pull mongo@sha256:099c76e2364be24f1a05da7adff073da7327585ccafb171fdaf9000aeb690dd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.473; amd64
	-	windows version 10.0.17763.2458; amd64

### `mongo:4-nanoserver` - windows version 10.0.20348.473; amd64

```console
$ docker pull mongo@sha256:dc804cc2cd89714e1f1c36cb58d1f003c42538b31fa1766a6931f479eecc9ab3
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358814425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fb352f632dae04505e9ceafa4c4a3edf74d429e5ecd7147c4a17665465c2594`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Sun, 16 Jan 2022 04:54:46 GMT
RUN Apply image ltsc2022-amd64
# Mon, 24 Jan 2022 23:22:08 GMT
SHELL [cmd /S /C]
# Mon, 24 Jan 2022 23:22:09 GMT
USER ContainerAdministrator
# Mon, 24 Jan 2022 23:22:27 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Jan 2022 23:22:28 GMT
USER ContainerUser
# Mon, 24 Jan 2022 23:32:34 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Mon, 24 Jan 2022 23:32:35 GMT
ENV MONGO_VERSION=4.4.12
# Mon, 24 Jan 2022 23:33:19 GMT
COPY dir:ddb807c26f1974dd41c054a2bef12ff55fc257bc9af1f055410eea9e996a8481 in C:\mongodb 
# Mon, 24 Jan 2022 23:33:36 GMT
RUN mongo --version && mongod --version
# Mon, 24 Jan 2022 23:33:37 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Jan 2022 23:33:38 GMT
EXPOSE 27017
# Mon, 24 Jan 2022 23:33:39 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:7691725ee3658d154f940d82fd8c3ff07c0dc589a0c9a93df47ed0ede92a76ab`  
		Size: 117.3 MB (117333150 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:af941a54762cda1c0e1e5ddbfe84c7d2f98e61a1f8ac9d819645377dd6d79003`  
		Last Modified: Tue, 25 Jan 2022 00:13:29 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349bf4556263f9c2b81ba296856d4ed419c51b44511c80012a51d9623732722c`  
		Last Modified: Tue, 25 Jan 2022 00:13:29 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5001cb7c0b016929260a25f63cdfc4d975053b0aad01932d3b1210673c87c78b`  
		Last Modified: Tue, 25 Jan 2022 00:13:27 GMT  
		Size: 83.6 KB (83556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24267e91ffbab34bda76a4360c00b630a61176344a205ee2f0a6bc7c06e18ce2`  
		Last Modified: Tue, 25 Jan 2022 00:13:27 GMT  
		Size: 1.1 KB (1136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c6d4b11520b61fa06a6215d786fb5bdaf12dcf75da502a70e5000b5a3849cf5`  
		Last Modified: Tue, 25 Jan 2022 00:31:41 GMT  
		Size: 263.5 KB (263489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7c63ec2e78d8c476e53beb51795893303b0979fb280d750771b10c865b826ca`  
		Last Modified: Tue, 25 Jan 2022 00:31:41 GMT  
		Size: 1.1 KB (1102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f427c5c94f61e9032f7416b32a4c2fc911f2ed33460097f4a9d13bb420c0c64e`  
		Last Modified: Tue, 25 Jan 2022 00:32:23 GMT  
		Size: 241.1 MB (241064515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e116036818820a66d65b61df43e895d2d217eeece7a941d836ec13b675f4d7d1`  
		Last Modified: Tue, 25 Jan 2022 00:31:39 GMT  
		Size: 61.7 KB (61652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd59e96341ffd5603be7d493ed0fe9db4217f2cb0825c083ec177d5587dd610`  
		Last Modified: Tue, 25 Jan 2022 00:31:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e74db3c06661d23b09b7504a6a59f1a2d3a1e8efe9299c1a68dc3ae7cdbbef`  
		Last Modified: Tue, 25 Jan 2022 00:31:38 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5709ad5066b2ef10b6a5eb6927f4f0916ee0d81d08b70f4d282efe4e58481071`  
		Last Modified: Tue, 25 Jan 2022 00:31:38 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:4-nanoserver` - windows version 10.0.17763.2458; amd64

```console
$ docker pull mongo@sha256:7659d5304bc72080d09d5269da78a2b8f370212bd6f3855f0338c5e5c1b5f94e
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.5 MB (344506469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab33e58b04cc452916bb3504cb3bab0834a67b52896c13400984bf4400b765a0`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Tue, 18 Jan 2022 01:20:34 GMT
RUN Apply image 1809-amd64
# Mon, 24 Jan 2022 23:24:23 GMT
SHELL [cmd /S /C]
# Mon, 24 Jan 2022 23:24:23 GMT
USER ContainerAdministrator
# Mon, 24 Jan 2022 23:24:38 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Mon, 24 Jan 2022 23:24:39 GMT
USER ContainerUser
# Mon, 24 Jan 2022 23:33:48 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Mon, 24 Jan 2022 23:33:49 GMT
ENV MONGO_VERSION=4.4.12
# Mon, 24 Jan 2022 23:34:40 GMT
COPY dir:ddb807c26f1974dd41c054a2bef12ff55fc257bc9af1f055410eea9e996a8481 in C:\mongodb 
# Mon, 24 Jan 2022 23:34:59 GMT
RUN mongo --version && mongod --version
# Mon, 24 Jan 2022 23:35:00 GMT
VOLUME [C:\data\db C:\data\configdb]
# Mon, 24 Jan 2022 23:35:01 GMT
EXPOSE 27017
# Mon, 24 Jan 2022 23:35:01 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:b5c97e1d373f591225559869af7f4f01399c201f89d21f903b1d23c830aa0a3f`  
		Size: 103.0 MB (103046552 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:fdb052c4016b3238a417abae6ce3a3c81e145118a4325ab2c01bba6cc9eedc3f`  
		Last Modified: Tue, 25 Jan 2022 00:19:35 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:239067809343d5f4e095b39624dfb9ca941d8dded1963d405cf946c066fc3988`  
		Last Modified: Tue, 25 Jan 2022 00:19:34 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49e4524972be3a240be3eceb5d9e1b0ba086c38be42fbd75d9a9eda4bbd6d716`  
		Last Modified: Tue, 25 Jan 2022 00:19:33 GMT  
		Size: 75.2 KB (75231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d41aa32bc9bad3c1aaf1a0eeddb9f7aa652e2114e669ad049b3935d95e7bd92`  
		Last Modified: Tue, 25 Jan 2022 00:19:32 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5974c0cdcac59d5825eddb11dde33d91ff93ec2e6d4fec50dec35b2e017fa0b1`  
		Last Modified: Tue, 25 Jan 2022 00:32:40 GMT  
		Size: 263.5 KB (263507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8fb0f3296d45503cf179457038e7a1faaac683fcff30b8d77897db329bf3f8f`  
		Last Modified: Tue, 25 Jan 2022 00:32:40 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:084d2822e27cb6e4f6187cacd8f15f971883f011507332678cf096f8f2b1df97`  
		Last Modified: Tue, 25 Jan 2022 00:37:40 GMT  
		Size: 241.1 MB (241064469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31529410e2f14907b963d07eaeff345f6b4146b08dad85301c42d3f1771c57eb`  
		Last Modified: Tue, 25 Jan 2022 00:32:38 GMT  
		Size: 48.6 KB (48629 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3fcd6dbf1dfbff6f69418540bb7aa0a162300ba68587e6abdb75e63c6389bec`  
		Last Modified: Tue, 25 Jan 2022 00:32:37 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b990d17f1b3f35efbfecbc2894d4c35e36dfd821f61c8ce9e2c15daeed3ccc6`  
		Last Modified: Tue, 25 Jan 2022 00:32:37 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb259f47a8cbbccc7d3694c9b056773cf180b931e4ddde553d51f2b98c030553`  
		Last Modified: Tue, 25 Jan 2022 00:32:38 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
