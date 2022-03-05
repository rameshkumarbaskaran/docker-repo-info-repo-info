## `openjdk:19-ea-jdk-nanoserver`

```console
$ docker pull openjdk@sha256:733133a9280724d8cfff6c3747ade5cbcfadffbc90c131dabcf9b3448adcec78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `openjdk:19-ea-jdk-nanoserver` - windows version 10.0.17763.2565; amd64

```console
$ docker pull openjdk@sha256:276db2d86339b63c8d220f04c88481a36aead9154efbb7071750031de60f4ddc
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294507913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f4cadd2ea4a5a05f3b741c64da25498c9b9b74d5b6b016e33053d87804a8fe`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 02 Feb 2022 19:06:51 GMT
RUN Apply image 1809-amd64
# Wed, 09 Feb 2022 18:45:32 GMT
SHELL [cmd /s /c]
# Wed, 09 Feb 2022 18:45:33 GMT
ENV JAVA_HOME=C:\openjdk-19
# Wed, 09 Feb 2022 18:45:33 GMT
USER ContainerAdministrator
# Wed, 09 Feb 2022 18:45:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Feb 2022 18:45:47 GMT
USER ContainerUser
# Fri, 04 Mar 2022 23:18:02 GMT
ENV JAVA_VERSION=19-ea+12
# Fri, 04 Mar 2022 23:18:16 GMT
COPY dir:ccbd27f613b007f80607fb4082df8303501b29f458636fc29f86897e41a47c46 in C:\openjdk-19 
# Fri, 04 Mar 2022 23:18:39 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Fri, 04 Mar 2022 23:18:40 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:bd0b37167cd3d731eb15196e123df7156b5a35597874d3016a1a4298c46fac3f`  
		Size: 103.1 MB (103087119 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:5a7f567e84a5a148036156650a47ef7eec0187f17e880d3b475e51dacd70077b`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e69acde47ea38ca917ac70bd099e8642e4d106e4d031254a5bd61c52e9e93a26`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a983d7a89070a62890b5312d217fb42c0a23a81f4b88020f86dd774b681bd5`  
		Last Modified: Wed, 09 Feb 2022 19:20:50 GMT  
		Size: 1.2 KB (1153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798ff236fae94b7a9651e0beb7fde720729c184b3d3150895ba4d507d0b4794b`  
		Last Modified: Wed, 09 Feb 2022 19:20:49 GMT  
		Size: 77.7 KB (77739 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b819309b74b4730666b4d3b76627010d142d418aa74b8068c4e4af5d3d77b23`  
		Last Modified: Wed, 09 Feb 2022 19:20:47 GMT  
		Size: 1.2 KB (1160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc231c52c8d168bbd41fe7240844509741af09d3c10d0947805819cef4f81733`  
		Last Modified: Fri, 04 Mar 2022 23:24:43 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ed1c81f2cc5bd0232fe8978897f17054540ae2588e0ecd7400e2e0b6fe99714`  
		Last Modified: Fri, 04 Mar 2022 23:25:03 GMT  
		Size: 187.8 MB (187780296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af5586b4e1e1143b45557dc152cd85c15e5645d0b6ca5c93a9155703677114b`  
		Last Modified: Fri, 04 Mar 2022 23:24:44 GMT  
		Size: 3.6 MB (3555807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b362b3b3f9d19e0e87970e75bcebb781fb9d1d422294236734ef9e04da7c311e`  
		Last Modified: Fri, 04 Mar 2022 23:24:43 GMT  
		Size: 1.2 KB (1152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
