## `openjdk:20-ea-6-nanoserver-1809`

```console
$ docker pull openjdk@sha256:5d5aa0f05bbd836d9494d9a2b0911efc43efacbd28ac8aaec68f735692a6dc28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.3165; amd64

### `openjdk:20-ea-6-nanoserver-1809` - windows version 10.0.17763.3165; amd64

```console
$ docker pull openjdk@sha256:015e6931a4a291bbef8828a28bc7ce61d01a5117b95cc6356a2a8bf9242ee05c
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.8 MB (298826453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f564a41c5d100c3979300218e927ed2a3dce5125155e306e54ed4bc894a43e2`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 06 Jul 2022 22:15:10 GMT
RUN Apply image 10.0.17763.3165
# Wed, 13 Jul 2022 14:50:41 GMT
SHELL [cmd /s /c]
# Wed, 13 Jul 2022 15:52:36 GMT
ENV JAVA_HOME=C:\openjdk-20
# Wed, 13 Jul 2022 15:52:37 GMT
USER ContainerAdministrator
# Wed, 13 Jul 2022 15:52:49 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 13 Jul 2022 15:52:50 GMT
USER ContainerUser
# Mon, 18 Jul 2022 19:27:33 GMT
ENV JAVA_VERSION=20-ea+6
# Mon, 18 Jul 2022 19:27:48 GMT
COPY dir:503096e870fe4f4125730ed1f1445c334557101c3f468e8e889cdac09d59ded4 in C:\openjdk-20 
# Mon, 18 Jul 2022 19:28:12 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 18 Jul 2022 19:28:13 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:5d24e1a2f5c566b0afb1e46fc24e5cec821c8ebf44220276a95a2b91f44a2f2a`  
		Size: 103.2 MB (103155009 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3b09c07c6aeead64423fdefc240fe2e1b6330c96732fd2705113030da84416be`  
		Last Modified: Mon, 18 Jul 2022 21:22:33 GMT  
		Size: 1.1 KB (1144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c94d05d6baacbfa68cfb2958f0965811612f86860a0e4f86c3742cdbfbc022`  
		Last Modified: Mon, 18 Jul 2022 21:22:32 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cae155d737666fa6fb6c74f820b3e7f2470d72055ea13febb624515fcec6e1f`  
		Last Modified: Mon, 18 Jul 2022 21:22:32 GMT  
		Size: 1.1 KB (1142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf301cbd6754860321dd411bf1baa15e0ba0f68154452e0ffb84915c2340f3f`  
		Last Modified: Mon, 18 Jul 2022 21:22:32 GMT  
		Size: 73.1 KB (73119 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb02d029b4db33c144b7edd2594c5c7df303b1ea68bf6135d5133634b910d307`  
		Last Modified: Mon, 18 Jul 2022 21:22:30 GMT  
		Size: 1.2 KB (1172 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72715c910e30700ea94f4deb8d856a76de5b5cee31ef6b179146d636bc94365f`  
		Last Modified: Mon, 18 Jul 2022 21:22:30 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cb97d7b9b63864e1daf21e43143b5218938332a2e0457d6a55c14f48c5f31a2`  
		Last Modified: Mon, 18 Jul 2022 21:22:53 GMT  
		Size: 191.9 MB (191896654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:449502e21aa4c0334307dd40df5c360dc6aadb484dfa976314dd50fdb27168c7`  
		Last Modified: Mon, 18 Jul 2022 21:22:31 GMT  
		Size: 3.7 MB (3694727 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:667b2cf9eee1501fc1dcc756bf3a7d86aa3fdb2bdb2c7ae18fc25a1987456cda`  
		Last Modified: Mon, 18 Jul 2022 21:22:30 GMT  
		Size: 1.2 KB (1178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
