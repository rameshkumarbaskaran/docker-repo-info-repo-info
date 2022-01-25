## `mongo:4-nanoserver-ltsc2022`

```console
$ docker pull mongo@sha256:51246940306003c9cb10943cfdf255856825d2428757a11f7b3b3b9735bf1594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.20348.473; amd64

### `mongo:4-nanoserver-ltsc2022` - windows version 10.0.20348.473; amd64

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
