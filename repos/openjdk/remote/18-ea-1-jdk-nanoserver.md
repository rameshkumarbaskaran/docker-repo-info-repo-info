## `openjdk:18-ea-1-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:c9e7e8e4c19d3528d3b35ee74da5fa8af684c10611503892949af24630018c14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `openjdk:18-ea-1-jdk-nanoserver` - windows version 10.0.17763.1999; amd64

```console
$ docker pull openjdk@sha256:cff83f94c43b73c47e240ed61b95cb4933e63842cfae65217604c83d394741eb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.3 MB (289327537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99faf4cfbe6c325389759a538796c5c7abf164178bfff7ce45d47890ae3667e9`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sun, 06 Jun 2021 04:04:04 GMT
RUN Apply image 1809-amd64
# Wed, 09 Jun 2021 16:52:42 GMT
SHELL [cmd /s /c]
# Mon, 14 Jun 2021 21:23:18 GMT
ENV JAVA_HOME=C:\openjdk-18
# Mon, 14 Jun 2021 21:23:21 GMT
USER ContainerAdministrator
# Mon, 14 Jun 2021 21:23:47 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Mon, 14 Jun 2021 21:23:49 GMT
USER ContainerUser
# Mon, 14 Jun 2021 21:23:51 GMT
ENV JAVA_VERSION=18-ea+1
# Mon, 14 Jun 2021 21:24:10 GMT
COPY dir:7023c5364303ffc476f7c8a4469f868cdcb3e0de25d74c96cff2bae601eaaa4d in C:\openjdk-18 
# Mon, 14 Jun 2021 21:24:35 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 14 Jun 2021 21:24:37 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e4800203e906d49fbdaf1eeab4de72f28796d5b9a1ea44f8d7461001cfa56614`  
		Size: 102.7 MB (102671454 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:acc28506464ab4d21eaffeb562876f3408463a46d298d12ded7ac0e3dd3c1bd6`  
		Last Modified: Wed, 09 Jun 2021 17:25:28 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a8aa554907fcec99de91851053bfbdcc543f546430c0a1c27a0354cf66ab24`  
		Last Modified: Mon, 14 Jun 2021 21:39:04 GMT  
		Size: 1.1 KB (1055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:912c2d7b4763a54931ac01e61f4d52cf9bdfbcb35903c8a29acbc422174b5197`  
		Last Modified: Mon, 14 Jun 2021 21:39:04 GMT  
		Size: 1.1 KB (1072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b175b01ffc1eae821eef4878d9ba8edc445669d64945462f128e7caa1a5cbb3`  
		Last Modified: Mon, 14 Jun 2021 21:39:04 GMT  
		Size: 67.8 KB (67770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:696d5b17d363cf6c1471c63b7fc24a3d3c36b15d702a96f0f4ce1cdf249db20f`  
		Last Modified: Mon, 14 Jun 2021 21:39:01 GMT  
		Size: 1.0 KB (1017 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d6491a2252be58c6767e034eb06f6bb5ccbb500997f5da2b7955740a151ad18`  
		Last Modified: Mon, 14 Jun 2021 21:39:01 GMT  
		Size: 1.1 KB (1050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:078ef194391f4d26400a910f5e3b9d9075bcc7999a6b2ad33c0fe7e4c0bcbaa8`  
		Last Modified: Mon, 14 Jun 2021 21:42:21 GMT  
		Size: 182.9 MB (182925926 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e8d513b5f309b86577081c9e90359630343bf6a4b2e47266daebdd343a234dc`  
		Last Modified: Mon, 14 Jun 2021 21:39:05 GMT  
		Size: 3.7 MB (3655889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f264dca24a97d76a3676aaedf0970e365f22665e881c7e5df11431e466b1888e`  
		Last Modified: Mon, 14 Jun 2021 21:39:01 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
