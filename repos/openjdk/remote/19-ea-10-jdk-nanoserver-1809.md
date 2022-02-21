## `openjdk:19-ea-10-jdk-nanoserver-1809`

```console
$ docker pull openjdk@sha256:e0ded282be4aad2ef2c795de2fa4939842254210614b2b1427a6d63f3678e818
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2565; amd64

### `openjdk:19-ea-10-jdk-nanoserver-1809` - windows version 10.0.17763.2565; amd64

```console
$ docker pull openjdk@sha256:c8c8dddb256d5ac04caf411aeee532da7e5e155fa4830362e564e0e767e3f207
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291695680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca4d26fb4b715c04a51473c43977632ffa29b3e7078519e1ca7a2019051575a8`
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
# Mon, 21 Feb 2022 18:18:57 GMT
ENV JAVA_VERSION=19-ea+10
# Mon, 21 Feb 2022 18:19:12 GMT
COPY dir:15c5c9a91214d2fa5c7395e4e4614c521a31fdb49a54ff031934d92e372b8632 in C:\openjdk-19 
# Mon, 21 Feb 2022 18:19:40 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Mon, 21 Feb 2022 18:19:41 GMT
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
	-	`sha256:4cd37f0eb0195c5b3339eb0b12d7e259d42bd35378fd152f1178452ee22dfe28`  
		Last Modified: Mon, 21 Feb 2022 19:25:04 GMT  
		Size: 1.0 KB (1028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b36b3d69852e88cee613c3c272e7ed9f2ade23875b4b571404160e27b69df2e`  
		Last Modified: Mon, 21 Feb 2022 19:25:24 GMT  
		Size: 185.0 MB (184996792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab24340bad9c7fb5f046f1b1be5329734971f36c494c8447815e4bd19e3b58d`  
		Last Modified: Mon, 21 Feb 2022 19:25:07 GMT  
		Size: 3.5 MB (3527276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e0a1bac649faeb6a5c6d3332ca97134daad95ff043e62e435023a09c2bbed84`  
		Last Modified: Mon, 21 Feb 2022 19:25:03 GMT  
		Size: 1.1 KB (1093 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
