## `openjdk:8-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e61638d99042b5426ff6d18b78768de3ed4272c91776d6737c130d619e7c8293
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `openjdk:8-jre-nanoserver-1809` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:47076fab343b2eeb8590a97c24bf734049f6eef9ea804f5aefd8277bf9b5e4c1
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141448345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88cad2645261af267f56b4f3327d53b4b1cb827182b41e4b3cd013dc2e14c81f`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Wed, 09 Mar 2022 17:35:05 GMT
ENV JAVA_HOME=C:\openjdk-8
# Wed, 09 Mar 2022 17:35:06 GMT
USER ContainerAdministrator
# Wed, 09 Mar 2022 17:35:15 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Mar 2022 17:35:16 GMT
USER ContainerUser
# Wed, 09 Mar 2022 17:35:16 GMT
ENV JAVA_VERSION=8u322
# Wed, 09 Mar 2022 17:37:53 GMT
COPY dir:f4c77e4259f68c5f890bc7ab442034fb0a5366735393f4c5400d26f276285797 in C:\openjdk-8 
# Wed, 09 Mar 2022 17:38:07 GMT
RUN echo Verifying install ... 	&& echo   java -version && java -version 	&& echo Complete.
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cae2b05f4b79e8fd3e173be31895e963d84f0cb359b7af88517005f3b2551c`  
		Last Modified: Wed, 09 Mar 2022 18:03:38 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34f76aeda459522891ce5c09a14366ca6902544816234ddde267328c41ab6087`  
		Last Modified: Wed, 09 Mar 2022 18:03:38 GMT  
		Size: 1.2 KB (1155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec184a8d491152de6c27a01be4a1aa687f007739313ba102635ef2a88f0fed22`  
		Last Modified: Wed, 09 Mar 2022 18:03:35 GMT  
		Size: 75.3 KB (75338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3244cd8eccd07203a24408e2adf77c5e0618c7f913e885d4f4b61f5f69926236`  
		Last Modified: Wed, 09 Mar 2022 18:03:35 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12d4724555dee6074a8f06014d9747a1321cdc874da9f0c383590a10b934966d`  
		Last Modified: Wed, 09 Mar 2022 18:03:35 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f62b1debb252fa31cfababa9c498be6b94ab96da33a8d6de4901a1cd005e4b`  
		Last Modified: Wed, 09 Mar 2022 18:04:44 GMT  
		Size: 38.3 MB (38265899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eeef775d95dab80f04114bbc779e77bb3476bd480585f5a6e103f18e11320c3`  
		Last Modified: Wed, 09 Mar 2022 18:04:37 GMT  
		Size: 46.8 KB (46799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
