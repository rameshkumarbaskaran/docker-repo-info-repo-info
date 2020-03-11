## `openjdk:11-jre-nanoserver-1809`

```console
$ docker pull openjdk@sha256:2029231735ff6915b86c37d08b450944205351656ab28f8880ac9173705a6df2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:11-jre-nanoserver-1809` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:ab4df62f3f2211254a027461fc3cefbcb4b480f95b771d2e3bd8678440ec19b6
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.1 MB (291074053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632cffb475be51db514e49c4a0caeb84b3d740401413807cf74164dd7b89bdea`
-	Default Command: `["c:\\windows\\system32\\cmd.exe"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:56:25 GMT
SHELL [cmd /s /c]
# Wed, 11 Mar 2020 15:11:38 GMT
ENV JAVA_HOME=C:\openjdk-11
# Wed, 11 Mar 2020 15:11:39 GMT
USER ContainerAdministrator
# Wed, 11 Mar 2020 15:11:59 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Mar 2020 15:12:00 GMT
USER ContainerUser
# Wed, 11 Mar 2020 15:12:01 GMT
ENV JAVA_VERSION=11.0.6
# Wed, 11 Mar 2020 15:13:01 GMT
COPY dir:dcc02c643f10bd08676197988d11abdf4d8aeda19e024c3b8c403d1d777f4b34 in C:\openjdk-11 
# Wed, 11 Mar 2020 15:15:06 GMT
RUN echo Verifying install ... 	&& echo   java --version && java --version
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a66be005a5120fc8bbc31290c77aa0e6580d02bc61948ef0602bf09a6ab61ba`  
		Last Modified: Wed, 11 Mar 2020 15:26:11 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fbb5f9a84bc35ae200c7e13f28372f1b097d1a4852daeca26867058b5481534`  
		Last Modified: Wed, 11 Mar 2020 15:34:33 GMT  
		Size: 840.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78c7e18f23e165b26fbb475890a15bbc28385ce67f1b2417057b7645e35daa2e`  
		Last Modified: Wed, 11 Mar 2020 15:34:33 GMT  
		Size: 841.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:915639190b3852a05629aaf1161baf071dd090aa7d90d0a946006f1eff482de3`  
		Last Modified: Wed, 11 Mar 2020 15:34:33 GMT  
		Size: 68.2 KB (68178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8afea8a5aec85996a4f215989da47f3d1ac9247e94be1dc792f10b49209e98ea`  
		Last Modified: Wed, 11 Mar 2020 15:34:30 GMT  
		Size: 934.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f99e8172e8f2bd203f9acd015d6335646cd93e27be5170fbbc8a90e26e06652`  
		Last Modified: Wed, 11 Mar 2020 15:34:30 GMT  
		Size: 929.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e340a7484dcbd308b10e89a3aa876326ace566a8a837cbcd199e4499b7113856`  
		Last Modified: Wed, 11 Mar 2020 15:34:54 GMT  
		Size: 189.9 MB (189905803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7240bfda501cf8e034599da941295149c6629666c511fed1a98efefd6d8c07b9`  
		Last Modified: Wed, 11 Mar 2020 15:35:44 GMT  
		Size: 45.4 KB (45350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
