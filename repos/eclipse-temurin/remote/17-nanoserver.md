## `eclipse-temurin:17-nanoserver`

```console
$ docker pull eclipse-temurin@sha256:830074b6c0b72fbf061acb8e4be67317cf452b55191b02b3208db1c891fbef4c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	windows version 10.0.20348.768; amd64
	-	windows version 10.0.17763.3046; amd64

### `eclipse-temurin:17-nanoserver` - windows version 10.0.20348.768; amd64

```console
$ docker pull eclipse-temurin@sha256:6d89b26767c6352f1a1044152e2bfa68997ecf14a033aed4bd42f4032dd09f39
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **303.3 MB (303331039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:308d3162567d55bad77c6da06540587d70de0ff13f48b658fd682adc3b165632`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 04:10:14 GMT
RUN Apply image 10.0.20348.768
# Wed, 15 Jun 2022 18:08:52 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 18:12:11 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 15 Jun 2022 18:12:11 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 Jun 2022 18:12:12 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 18:12:25 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 18:12:25 GMT
USER ContainerUser
# Wed, 15 Jun 2022 18:12:42 GMT
COPY dir:79e149bb8ddfd2a6f3a6975343033743c253d84c3b058ff83fe3162d456d08dd in C:\openjdk-17 
# Wed, 15 Jun 2022 18:12:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jun 2022 18:13:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:fca88290e1b048d74ec4e9d1548c4ec09dc3921f80285f39a186278fcaf2d86f`  
		Size: 118.0 MB (117976537 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:60cbdb7704dc53714205f32082d3faa20d7c93a53c40cb88f22581e85a2943fc`  
		Last Modified: Wed, 15 Jun 2022 19:13:47 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a85dc5bea571322c1bad47fce6713544feadbd57c610238fe102b9e016782f77`  
		Last Modified: Wed, 15 Jun 2022 19:21:16 GMT  
		Size: 1.1 KB (1110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6355b8f9281a8e613addd72358ba79771b42c4aa2c9f5d78a4e165ab488f4abc`  
		Last Modified: Wed, 15 Jun 2022 19:21:16 GMT  
		Size: 1.1 KB (1062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3eba0c7671dae4bc67f14fedc7eb347e929af8e3c986b4f3814212765626b5e`  
		Last Modified: Wed, 15 Jun 2022 19:21:16 GMT  
		Size: 1.1 KB (1061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d777afa6595897951b2a381ba52647b2c30d3b3bdecd401e1108b98ad28965af`  
		Last Modified: Wed, 15 Jun 2022 19:21:13 GMT  
		Size: 85.2 KB (85203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca232dfebb8819191df3bd8cc594d7006e50f460ed206f357249bd8ce618539f`  
		Last Modified: Wed, 15 Jun 2022 19:21:14 GMT  
		Size: 1.1 KB (1057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a11eb6cdc790c0b3f5ed3056bbd89b0909dfd80b4af13a33a1c9aa62d7b754f`  
		Last Modified: Wed, 15 Jun 2022 19:21:35 GMT  
		Size: 185.2 MB (185200880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c04c311eceb1c375badeb5353f36e3d7227fc89b0c1626d0606e1aa3ec9902`  
		Last Modified: Wed, 15 Jun 2022 19:21:13 GMT  
		Size: 61.8 KB (61838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792c80d5427f2a5c5249cb85939a79baaf836d013389c93ba8fe3b3ba9ef48fd`  
		Last Modified: Wed, 15 Jun 2022 19:21:13 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:17-nanoserver` - windows version 10.0.17763.3046; amd64

```console
$ docker pull eclipse-temurin@sha256:22f0909283474c8598036c7b23bff8a23ef89ffac88bc22253dfc2af90b85811
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **292.1 MB (292077109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:815eebe70986474a1123d1adfa8923f994368931b08507b78c8de5705e89c6a3`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 09 Jun 2022 19:20:11 GMT
RUN Apply image 10.0.17763.3046
# Wed, 15 Jun 2022 17:30:58 GMT
SHELL [cmd /s /c]
# Wed, 15 Jun 2022 17:51:13 GMT
ENV JAVA_VERSION=jdk-17.0.3+7
# Wed, 15 Jun 2022 17:51:14 GMT
ENV JAVA_HOME=C:\openjdk-17
# Wed, 15 Jun 2022 17:51:15 GMT
USER ContainerAdministrator
# Wed, 15 Jun 2022 17:51:26 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH%     && setx /M PATH %JAVA_HOME%\bin;%PATH%     && echo Complete.
# Wed, 15 Jun 2022 17:51:27 GMT
USER ContainerUser
# Wed, 15 Jun 2022 17:51:43 GMT
COPY dir:79e149bb8ddfd2a6f3a6975343033743c253d84c3b058ff83fe3162d456d08dd in C:\openjdk-17 
# Wed, 15 Jun 2022 17:51:59 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 15 Jun 2022 17:52:00 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d555a7e4de4dd775379d5c43c1419374bff7908670dc7444be5e8e8f386f3d26`  
		Size: 103.2 MB (103153235 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:92b4c385cd5cbb12fb09cb31c12b5e5de38cf7b380c8681286caac242c06d3ed`  
		Last Modified: Wed, 15 Jun 2022 18:22:11 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2865d234ceed85c5d08eaade8ec8df736ee993320a714700398635fe2a06c3`  
		Last Modified: Wed, 15 Jun 2022 18:48:04 GMT  
		Size: 1.2 KB (1158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4951a030dcae3a9c8fc8e42d359bdd193840dd8c51fb43602fa8cedd1ab20539`  
		Last Modified: Wed, 15 Jun 2022 18:48:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d66be3747421813004728c4a8a2d307e746f0bbe2f3b027803803cbe8456461`  
		Last Modified: Wed, 15 Jun 2022 18:48:04 GMT  
		Size: 1.2 KB (1166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87368c9a474994883fe6a9f054ad1867ddac8a838f4c66e17963ebbef448337`  
		Last Modified: Wed, 15 Jun 2022 18:48:01 GMT  
		Size: 71.0 KB (71012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbe5faaba8854bd5aad06eb3c7f4707d2fcd8c586462977ed2492148615fd7f0`  
		Last Modified: Wed, 15 Jun 2022 18:48:01 GMT  
		Size: 1.2 KB (1170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c87ef1d523f7bd9c830a7ce9106c09c1dee232b5b99391453e09d4d4d11dba3`  
		Last Modified: Wed, 15 Jun 2022 18:51:17 GMT  
		Size: 185.2 MB (185192851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84d2411137c9c1c4488e54edee490fd090ea75c35e4fdce51e2bd66cd3d4ff09`  
		Last Modified: Wed, 15 Jun 2022 18:48:05 GMT  
		Size: 3.7 MB (3653028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5930683dd74b26a8705fa99c08194692831d9633e0d8b2132cc62dfdbd509f`  
		Last Modified: Wed, 15 Jun 2022 18:48:01 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
