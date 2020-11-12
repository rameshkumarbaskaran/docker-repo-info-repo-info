## `openjdk:11-nanoserver-1809`

```console
$ docker pull openjdk@sha256:d8deaef1fa5b5d4221147b5034b5576da1fab654aa25458e2a4ca1228deedc07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `openjdk:11-nanoserver-1809` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:028cbdce6a29174a9953b6bc5a97df1a9ba5227b7d9ac434d1edf0cf607f0d14
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292078805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:493cb31a9d46a1260025b489e79d118ec584508c7a55fdaae8a3dd76ac455e9c`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Sat, 31 Oct 2020 05:10:43 GMT
RUN Apply image 1809-amd64
# Wed, 11 Nov 2020 17:53:16 GMT
SHELL [cmd /s /c]
# Wed, 11 Nov 2020 18:09:02 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Nov 2020 18:09:03 GMT
USER ContainerAdministrator
# Wed, 11 Nov 2020 18:09:13 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Nov 2020 18:09:14 GMT
USER ContainerUser
# Thu, 12 Nov 2020 01:30:02 GMT
ENV JAVA_VERSION=11.0.9.1
# Thu, 12 Nov 2020 01:30:40 GMT
COPY dir:970d34e376da5a0c6fb3cec9f25ccfd1dae852609db145ba03fc6119961e6f7c in C:\openjdk-11 
# Thu, 12 Nov 2020 01:31:05 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Thu, 12 Nov 2020 01:31:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:f1b217fe8837d4d85cb8228a52344d3504d7aa51ba30167a20a6a4cb80cdcaa0`  
		Size: 101.3 MB (101279682 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:41b7be9dc08821cf81d29b16e0df54f7f3e3aeaa6407f43520c6259f2d84b10c`  
		Last Modified: Wed, 11 Nov 2020 18:27:27 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:304a4001d0ea6e189886c6d378cc1dfa593e80a729c1623f21cd2b9013ba46ad`  
		Last Modified: Wed, 11 Nov 2020 18:32:21 GMT  
		Size: 864.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82c7a43773efd42ef79b3edb7790d24e0faece36d5d28220e1d6392fdf19ca9`  
		Last Modified: Wed, 11 Nov 2020 18:32:20 GMT  
		Size: 871.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d19ea44bc4fdbf45f644cb6e7c48f9b89767c8eddbb9918c90a3570eb885e9e`  
		Last Modified: Wed, 11 Nov 2020 18:32:20 GMT  
		Size: 66.3 KB (66350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee33ec85133ca14a34431b91b04beb43b8977c8c14fac31f99050b03d8b0fa63`  
		Last Modified: Wed, 11 Nov 2020 18:32:17 GMT  
		Size: 892.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce33ca42365808898863471e20f3d2f0cf6da0b0e254371694a12e781957ebf`  
		Last Modified: Thu, 12 Nov 2020 01:52:36 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb237d30d56256d56f07378883869304e782c5cbbd7143b29f8f5bb78ca4b1a4`  
		Last Modified: Thu, 12 Nov 2020 01:52:54 GMT  
		Size: 190.6 MB (190649123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd1c3ab03ea7b84c3ac967f93825ae21d489a9cd50368eeb4e481b12cddc6370`  
		Last Modified: Thu, 12 Nov 2020 01:52:36 GMT  
		Size: 78.4 KB (78419 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274cc24b8502386b50ec89cc71cd5cd7cb3307a553a79e0c775638a0ba2dee8f`  
		Last Modified: Thu, 12 Nov 2020 01:52:36 GMT  
		Size: 887.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
