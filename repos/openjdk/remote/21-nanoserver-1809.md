## `openjdk:21-nanoserver-1809`

```console
$ docker pull openjdk@sha256:6da774d4eaf3826b5dca80b73bcbcb35bfb7a4049dbbfbd8c2f45fc09b70f8a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4131; amd64

### `openjdk:21-nanoserver-1809` - windows version 10.0.17763.4131; amd64

```console
$ docker pull openjdk@sha256:d6d389b94bceca8582c2ac606db85fb0ab6b70d498bd70ef16087d4deeb6cf6a
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306622710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:690351dc0e41a33a08c333f001550c1975eb58d2aed29d76690d5ab030a08c92`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 11 Mar 2023 10:09:02 GMT
RUN Apply image 10.0.17763.4131
# Thu, 16 Mar 2023 00:45:50 GMT
SHELL [cmd /s /c]
# Thu, 16 Mar 2023 04:21:31 GMT
ENV JAVA_HOME=C:\openjdk-21
# Thu, 16 Mar 2023 04:21:32 GMT
USER ContainerAdministrator
# Thu, 16 Mar 2023 04:21:44 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Thu, 16 Mar 2023 04:21:45 GMT
USER ContainerUser
# Tue, 21 Mar 2023 00:19:39 GMT
ENV JAVA_VERSION=21-ea+14
# Tue, 21 Mar 2023 00:19:56 GMT
COPY dir:2476afd2956a2e140575c65fcc10668d1e8d9ef3841e80df8d88d3adc35fadc2 in C:\openjdk-21 
# Tue, 21 Mar 2023 00:20:32 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Tue, 21 Mar 2023 00:20:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:95eb2f0f3287f5ec687287cc244924aafc74c7ada3121d43f54223487f3f2d8d`  
		Last Modified: Thu, 16 Mar 2023 01:43:14 GMT  
		Size: 106.7 MB (106684240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b5837fe68a36caddf38b0aaa99f4ef20ca36d8dfe2825fa6ffbcf0d38b9d59a`  
		Last Modified: Thu, 16 Mar 2023 01:42:43 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450d272e24dcd824ed0a2cfaab457791740701be7e655050f5a344dba0111120`  
		Last Modified: Thu, 16 Mar 2023 04:32:07 GMT  
		Size: 1.1 KB (1141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:375c9b367947b6469eed8f3b494a27778599dd1e8ab85682d96eee96a8d38097`  
		Last Modified: Thu, 16 Mar 2023 04:32:07 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d48b42b9c3192f6ddd8ce43c9c7a2c8b1fb3f906fe4eea3aa9b1e4fc28b4161`  
		Last Modified: Thu, 16 Mar 2023 04:32:08 GMT  
		Size: 72.2 KB (72190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44544dc6ee19ff5b39d3756cbc6d53830c65429f0d1ad05b8422c3c33ac8311`  
		Last Modified: Thu, 16 Mar 2023 04:32:05 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5c2d99daf0d105fe4dd6af15b2ada03feeb8101e302366cbaad0caffd24ef5e`  
		Last Modified: Tue, 21 Mar 2023 00:23:23 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e065285438c8ae13d54e7646657ea2c11a753b6689e103c68436fce1c3b43b7`  
		Last Modified: Tue, 21 Mar 2023 00:23:45 GMT  
		Size: 196.1 MB (196083991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38fcc52ccec9bbe8694ad5b098b73bfd60d79f4e30981a44ea5b79e336c1adba`  
		Last Modified: Tue, 21 Mar 2023 00:23:24 GMT  
		Size: 3.8 MB (3775374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1448f10be757d7d8f8a72916e0b37a4eea8ceda33e5c8cf3fccc7e7abd894c76`  
		Last Modified: Tue, 21 Mar 2023 00:23:23 GMT  
		Size: 1.2 KB (1169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
