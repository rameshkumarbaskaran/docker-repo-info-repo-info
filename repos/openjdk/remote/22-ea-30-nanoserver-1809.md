## `openjdk:22-ea-30-nanoserver-1809`

```console
$ docker pull openjdk@sha256:af15bca4b754388895e952be7952f2c7e67054da45eacf43b27ad3a5ae413795
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.5206; amd64

### `openjdk:22-ea-30-nanoserver-1809` - windows version 10.0.17763.5206; amd64

```console
$ docker pull openjdk@sha256:81d4d7685239b72f1a67a8472b968935422ea5b4f81b08ec70d6758ae0fa033f
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305753666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd72dd6c52aeaa617d3d1cfad1bb77c26607fe1654e4721f1ce6c133020f432a`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Mon, 04 Dec 2023 10:54:04 GMT
RUN Apply image 10.0.17763.5206
# Tue, 09 Jan 2024 03:48:20 GMT
SHELL [cmd /s /c]
# Tue, 09 Jan 2024 03:48:21 GMT
ENV JAVA_HOME=C:\openjdk-22
# Tue, 09 Jan 2024 03:48:21 GMT
USER ContainerAdministrator
# Tue, 09 Jan 2024 03:48:34 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Tue, 09 Jan 2024 03:48:34 GMT
USER ContainerUser
# Tue, 09 Jan 2024 03:48:34 GMT
ENV JAVA_VERSION=22-ea+30
# Tue, 09 Jan 2024 03:48:44 GMT
COPY dir:5f6175456bd75036441df77ae70a347d5f61c8c5d6826fd50ec6962633347072 in C:\openjdk-22 
# Tue, 09 Jan 2024 03:48:50 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 09 Jan 2024 03:48:50 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:424f13a93a185a5defe848e7d270655e05233555f51328c0af24b9e70677d037`  
		Last Modified: Tue, 12 Dec 2023 20:02:40 GMT  
		Size: 104.5 MB (104510104 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2819a84c776fd4c8565719298aa308d470cb65c5f273e1edfa95e6553f77b637`  
		Last Modified: Tue, 09 Jan 2024 03:48:57 GMT  
		Size: 1.1 KB (1103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b467df36291f203a5a0d03341dc7e13cac82b9a9ab354ac00ff504a56903b9fc`  
		Last Modified: Tue, 09 Jan 2024 03:48:56 GMT  
		Size: 1.0 KB (1038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b529f68fdafc06b3980b462ca54e5b27b049ca4febce0787460446013f42146`  
		Last Modified: Tue, 09 Jan 2024 03:48:56 GMT  
		Size: 1.0 KB (1035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b2882b7e8186623ee2da47dc010e7a9178b294b19ec85405271af0f7514ec36`  
		Last Modified: Tue, 09 Jan 2024 03:48:56 GMT  
		Size: 66.5 KB (66509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bf020a350cc1c6b06cc6f0320c7836b1f61e55ac84f6376f08734ed4332d135`  
		Last Modified: Tue, 09 Jan 2024 03:48:54 GMT  
		Size: 1.0 KB (1043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e823baa9197b2039c4118e86f082e0f4bf5973dbeb4ae8c3ccf7e182ed1e54b`  
		Last Modified: Tue, 09 Jan 2024 03:48:54 GMT  
		Size: 1.0 KB (1037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adbf9240b8e9dfa9d53509d0db831bd526efbb9322e9b29b3dc252dfc62cfec6`  
		Last Modified: Tue, 09 Jan 2024 03:49:05 GMT  
		Size: 197.3 MB (197334023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b627515a950a75184a5316c9a73b96742855bd6c2a199d4c168aa3832cbffd13`  
		Last Modified: Tue, 09 Jan 2024 03:48:55 GMT  
		Size: 3.8 MB (3836734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87a62bb00584052fe4f037a95916d243c266e3a0a49e3fef55ca1f76143facfa`  
		Last Modified: Tue, 09 Jan 2024 03:48:54 GMT  
		Size: 1.0 KB (1040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
