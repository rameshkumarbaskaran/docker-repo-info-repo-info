## `openjdk:11-jre-nanoserver`

```console
$ docker pull openjdk@sha256:c3c84f8d94aac49b40b5291f2ea50a5c67cefe62ba9db59789f1ec0476f717d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1577; amd64

### `openjdk:11-jre-nanoserver` - windows version 10.0.17763.1577; amd64

```console
$ docker pull openjdk@sha256:36ef5e84f8398550947c1ca3f7a052060bec8ffc3e8d6768dadc32aeea4195b9
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140734505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0f96b0a2df7a456b3ddd87028aa317da32a7357bf8533583c731bab58f17b7`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
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
# Thu, 12 Nov 2020 01:34:12 GMT
COPY dir:eaef7c5ff292e1f8a6aa3c608a2a96aef7062e71406091a23afb53db379465e6 in C:\openjdk-11 
# Thu, 12 Nov 2020 01:34:28 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version
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
	-	`sha256:40ad51179ec08f164e022e3eb9a698490c1947339f7bb425c1f8c09380a05976`  
		Last Modified: Thu, 12 Nov 2020 01:54:59 GMT  
		Size: 39.3 MB (39306540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:760b39c2df15dc20d714f479593e968af6a951d55162645a0f01dacdd2f3516b`  
		Last Modified: Thu, 12 Nov 2020 01:54:16 GMT  
		Size: 77.6 KB (77589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
