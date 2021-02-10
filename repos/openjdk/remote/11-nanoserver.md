## `openjdk:11-nanoserver`

```console
$ docker pull openjdk@sha256:6c3237ff47d3625e285b47dcd7faab45ddd45cf77affc225f477439b60bd0637
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1757; amd64

### `openjdk:11-nanoserver` - windows version 10.0.17763.1757; amd64

```console
$ docker pull openjdk@sha256:8a574697f06c4f17f47c6235401e4de8e260a7bda44ed67075e2789a56ec938d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.4 MB (292420607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad550c57ae5b5e1b541d11a726c58b9dbf0b33db96835e5f6f3fd71570d837e5`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Tue, 02 Feb 2021 13:06:30 GMT
RUN Apply image 1809-amd64
# Wed, 10 Feb 2021 16:45:48 GMT
SHELL [cmd /s /c]
# Wed, 10 Feb 2021 17:02:27 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 10 Feb 2021 17:02:28 GMT
USER ContainerAdministrator
# Wed, 10 Feb 2021 17:02:39 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 10 Feb 2021 17:02:39 GMT
USER ContainerUser
# Wed, 10 Feb 2021 17:02:39 GMT
ENV JAVA_VERSION=11.0.10
# Wed, 10 Feb 2021 17:02:52 GMT
COPY dir:c55c8a7ac9bf87302336a84fe1caa0b79ec42696e5d6969bc177cd9d6262fe26 in C:\openjdk-11 
# Wed, 10 Feb 2021 17:03:08 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 10 Feb 2021 17:03:08 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:ba17af31b9276ee11fdf859681b442db50979a39eff4cea2a559a5755cedbe01`  
		Size: 101.4 MB (101406193 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:89effbaeeb74323a670701c3b9dac248927e603ffb2d7efed14d993d32f7c183`  
		Last Modified: Wed, 10 Feb 2021 17:17:35 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33d69e485c1fb117d4a19befebc23e6e687fdeb40f5f6f782180950cce77cb77`  
		Last Modified: Wed, 10 Feb 2021 17:37:16 GMT  
		Size: 1.1 KB (1089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9507bbe9d84348cbd57ae7fc26b79ded1a0b2785c041498245dcf36daeee7119`  
		Last Modified: Wed, 10 Feb 2021 17:37:16 GMT  
		Size: 1.1 KB (1071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e313f63aa5e060761cf771925f99ddf177a2c6dee72bc959581a3537e9763fc`  
		Last Modified: Wed, 10 Feb 2021 17:37:16 GMT  
		Size: 65.2 KB (65243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca454fe52c8ab2372f9d5da017eeac37c02ff2075fd32c59134425273574c05f`  
		Last Modified: Wed, 10 Feb 2021 17:37:13 GMT  
		Size: 1.1 KB (1080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45a034d955055fe31e25205800d483063dc8f6070cfee295a78dff40662432c3`  
		Last Modified: Wed, 10 Feb 2021 17:37:13 GMT  
		Size: 1.1 KB (1074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d277b05feb9600a65d680cb7e053f04576df06af7a663e4c28a08b4a88a5274f`  
		Last Modified: Wed, 10 Feb 2021 17:37:31 GMT  
		Size: 190.9 MB (190852935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f4342978d01ffa091ec4b5a6d00d6947fba45931783e86fe555cc81870f3f79`  
		Last Modified: Wed, 10 Feb 2021 17:37:13 GMT  
		Size: 89.7 KB (89722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:634a4a4bf5fc905be85d88d71a59f5a70c588829e4ac1ea5c78f815946aec6e4`  
		Last Modified: Wed, 10 Feb 2021 17:37:13 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
