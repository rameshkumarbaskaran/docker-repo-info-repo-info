## `openjdk:21-nanoserver`

```console
$ docker pull openjdk@sha256:d6a739206ab560e1f28e8352866bea3ef4b062e0fd0ef306d3ab9efe99ac32ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4737; amd64

### `openjdk:21-nanoserver` - windows version 10.0.17763.4737; amd64

```console
$ docker pull openjdk@sha256:b217d68b1ed415b075dadc70e54d63d9c138fa12ccb6b5ad051affd46c7be704
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.4 MB (306388455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be63f9657cce1514d061459236fb60d40930d421f8fc10f247d575b87d1c19d4`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Aug 2023 08:33:47 GMT
RUN Apply image 10.0.17763.4737
# Wed, 09 Aug 2023 23:39:50 GMT
SHELL [cmd /s /c]
# Thu, 10 Aug 2023 02:47:12 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 10 Aug 2023 02:47:13 GMT
USER ContainerAdministrator
# Thu, 10 Aug 2023 02:47:23 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 10 Aug 2023 02:47:23 GMT
USER ContainerUser
# Thu, 10 Aug 2023 02:47:24 GMT
ENV JAVA_VERSION=21-ea+34
# Thu, 10 Aug 2023 02:47:39 GMT
COPY dir:126ff8951f9bbf5674d101616b5f2446db8fd119962bcdeb4c41f4d89b400077 in C:\openjdk-21 
# Thu, 10 Aug 2023 02:47:51 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Thu, 10 Aug 2023 02:47:51 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:86fab75eb466cadf89d853682179b3b57eba9fe28c78041dd52bced81e18a627`  
		Last Modified: Tue, 08 Aug 2023 17:55:54 GMT  
		Size: 104.5 MB (104459386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7e08c5247c8c7d832882da17ac85015e9dd4d4dfc9e4114fc14746eb2abded`  
		Last Modified: Thu, 10 Aug 2023 00:21:01 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3434ed9deffc375ad0cb38e443dc5fc1360d844968c96f2b511ba8ea8d59c0f4`  
		Last Modified: Thu, 10 Aug 2023 02:52:12 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e54f8430a84d34adc8f8adefa5c8bdf90fee0c09900855cd07da50d6010c2fec`  
		Last Modified: Thu, 10 Aug 2023 02:52:12 GMT  
		Size: 1.1 KB (1085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a23bc62e51ea7bc2fecb15f3693ab4a41cbdcc4acfebd18e8dd6c5f5ce9c9ea`  
		Last Modified: Thu, 10 Aug 2023 02:52:12 GMT  
		Size: 69.7 KB (69701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:520aa82f2ac0e8998feb41298f7ff989a63d8da7cdea2c2e926533fe6db48c20`  
		Last Modified: Thu, 10 Aug 2023 02:52:10 GMT  
		Size: 1.0 KB (1027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7be556f9e399777156172341a61a89107d7cb9e942898609effbf94882798473`  
		Last Modified: Thu, 10 Aug 2023 02:52:10 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c80f8297575d442a8935156d9d9541d6ce4fefd8f1ee00c4824936ecd6b31ae`  
		Last Modified: Thu, 10 Aug 2023 02:52:30 GMT  
		Size: 198.0 MB (198036356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e515ed035bbd395972ae6f672876c148945eed4ad691b9ddb06db0bc83cfb38`  
		Last Modified: Thu, 10 Aug 2023 02:52:11 GMT  
		Size: 3.8 MB (3816559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e17f792f34b786b4b1e8979c198e97e68c1e2e0a5788a0261411752336d9eed`  
		Last Modified: Thu, 10 Aug 2023 02:52:10 GMT  
		Size: 1.1 KB (1063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
