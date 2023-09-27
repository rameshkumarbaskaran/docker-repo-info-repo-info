## `openjdk:22-ea-nanoserver`

```console
$ docker pull openjdk@sha256:97a32d57dd6de7ae0870b0f9cb3eaaf3fe13e676e393a1762bd475ce3ec30a37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4851; amd64

### `openjdk:22-ea-nanoserver` - windows version 10.0.17763.4851; amd64

```console
$ docker pull openjdk@sha256:b56809ce46def75b3a5189af3597afe032c44b0996f59df6ad3d6ae685e66228
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **307.5 MB (307517390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85e22e76c94ba5a1456674bddf30a86ecbc66a49dffacb0a1e8f6a986cb1fa5d`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 29 Aug 2023 16:42:02 GMT
RUN Apply image 10.0.17763.4851
# Wed, 13 Sep 2023 02:29:44 GMT
SHELL [cmd /s /c]
# Wed, 13 Sep 2023 05:19:19 GMT
ENV JAVA_HOME=C:\openjdk-22
# Wed, 13 Sep 2023 05:19:19 GMT
USER ContainerAdministrator
# Wed, 13 Sep 2023 05:19:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Sep 2023 05:19:25 GMT
USER ContainerUser
# Wed, 27 Sep 2023 00:19:41 GMT
ENV JAVA_VERSION=22-ea+16
# Wed, 27 Sep 2023 00:19:56 GMT
COPY dir:c3e769279294543a655942c43301009a4a5e8e6983f8dab12cf6f4143dbe213a in C:\openjdk-22 
# Wed, 27 Sep 2023 00:20:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 27 Sep 2023 00:20:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:17ba6b878467260559b72cb6f7e79c829eae67862a09efe87f6dc324f49fc086`  
		Last Modified: Tue, 12 Sep 2023 18:31:40 GMT  
		Size: 104.5 MB (104492504 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7a5bcbc9b0f0398bf8f14c235b24ba85d9acacf855518119cd1ce338a235a15`  
		Last Modified: Wed, 13 Sep 2023 03:36:33 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6f344751fdeca77c774720f1f5845e2a683d1ed1b251bd6e554f91ab03d2b0`  
		Last Modified: Wed, 13 Sep 2023 05:26:46 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71be8c52d7c546ce325f7f3606c55b22e94fd1925aba26440028f33d2a873ff1`  
		Last Modified: Wed, 13 Sep 2023 05:26:46 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de794e4f653951d19d788489e6c197cbbaa2864a36a169d068b25cf13ea0c6a6`  
		Last Modified: Wed, 13 Sep 2023 05:26:46 GMT  
		Size: 79.5 KB (79476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4673df9416ca713de65ecb18e35ecfcad8bafedd6b1e61dca148de841d138b7`  
		Last Modified: Wed, 13 Sep 2023 05:26:44 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b93e5df64d64a14a4374e2fe98c2374b8bdda332d8560469c9ecbcfdf325922`  
		Last Modified: Wed, 27 Sep 2023 00:22:08 GMT  
		Size: 1.0 KB (1029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e83b5dbc845dc285bced65ea3607e9ce0335a717e0753ccf2c3d0c0e738c6383`  
		Last Modified: Wed, 27 Sep 2023 00:22:27 GMT  
		Size: 199.1 MB (199123395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbb3be2db015bc7e6100f643aa2270acd422a51b65243a244f54c46a0f34d16`  
		Last Modified: Wed, 27 Sep 2023 00:22:10 GMT  
		Size: 3.8 MB (3815287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a792845128f641b7eaec76d7ec553930fa52591381c21c4677f282c80c6319`  
		Last Modified: Wed, 27 Sep 2023 00:22:08 GMT  
		Size: 1.0 KB (1030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
